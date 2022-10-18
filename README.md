{{ Form::select('review_status', config('values.progress'), old('review_status', $review->review_status), ['class' => 'form-control mr-2 height-44']) }}
        @if(request()->query('is_complete') == 'true')
         {{ Form::button('更新', ['class' => 'btn-ucar-main green max-width-100 disabled']) }}
       @else
         {{ Form::submit('更新', ['class' => 'btn-ucar-main green max-width-100']) }}
       @endif


 <Mở thẻ a> class="btn btn-sm btn-primary" href="{{ route('shop.reviews.edit', [$item->id, 'is_complete' => 'true']) }}">詳細 <Đóng thẻ a >


 link trên url
http://127.0.0.1:8000/shop/reviews/807/edit?is_complete=true
