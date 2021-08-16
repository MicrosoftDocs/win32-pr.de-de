---
description: Eine statische Erstellerfunktion, die einen XamlUIPresenter für eine Renderoberfläche in einer Desktop-App erstellen kann.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: 247d676e3e2c85404f96324b1d78e1cd6ec2ab2159092d9a66717b2653ee5a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323433"
---
# <a name="createxamluipresenter-function"></a>CreateXamlUIPresenter-Funktion

Eine statische Erstellerfunktion, die einen [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) für eine Renderoberfläche in einer Desktop-App erstellen kann.

## <a name="syntax"></a>Syntax


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPresentSite* \[ In\]
</dt> <dd>

Eine vorhandene Hostingschnittstelle. Weitere Informationen finden Sie in Internet Explorer Dokumentation unter **IViewObjectPresentNotifySite.**

</dd> <dt>

*ppPresenter* \[ out\]
</dt> <dd>

Die **\[ \] exclusiveto-Schnittstelle** für einen [**XamlUIPresenter.**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **Standard-HResult,** **S \_ OK** für erfolg.

## <a name="remarks"></a>Hinweise

Zum Aufrufen dieser Methode ist ein **DllImport** von Windows.UI.Xaml.dll erforderlich.

Sie können diese Methode nicht über eine Windows Store-App aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows.ui.xaml-coretypes.idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
