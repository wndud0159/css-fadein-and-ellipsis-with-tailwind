# css-fadein-and-ellipsis-with-tailwind


.fadein {
  position: relative;
  overflow: hidden;
  animation: fadein 1s ease-in-out;
}

@keyframes fadein {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}

.ellipsis {
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}

.flex-ellipsis {
  @apply min-w-0 text-ellipsis whitespace-nowrap overflow-hidden;
}

.scrollx {
  overflow-x: scroll;
  /* IE scroll 숨김 */
  -ms-overflow-style: none;
}

.scrollx::-webkit-scrollbar {
  display: none;
  width: 0 !important;
}


<div className={`${wrapperClassName} flex items-center  min-w-0`}>
      {isCheckbox && (
        <div>
          <input
            onChange={onChange}
            disabled={disabled}
            type="checkbox"
            className={`${inputClassName} mr-3 accent-iback-primary border-iback-primary`}
            checked={isChecked}
          />
        </div>
      )}
      <div
        className={`${labelClassName} ${
          isEllipsis && 'text-ellipsis whitespace-nowrap overflow-hidden'
        }`}>
        <label className={` `}>{text}</label>
        {arrayText.length > 0 && arrayText.map((text, index) => <div key={index}>{text}</div>)}
      </div>
    </div>
    
    
    <meta name="title" property="og:title" content="" />
    <meta name="description" property="og:description" content=""/>
    <meta name="image" property="og:image" content="%PUBLIC_URL%/logo.png" /> 
    <meta name="url" property="og:url" content="" />

