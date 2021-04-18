---
description: Eine statische erstellerfunktion, die einen xamluipresenter für eine Renderoberfläche in einer Desktop-App erstellen kann.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Funktion "kreatexamluipresenter"
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
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365438"
---
# <a name="createxamluipresenter-function"></a>Funktion "kreatexamluipresenter"

Eine statische erstellerfunktion, die einen [**xamluipresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) für eine Renderoberfläche in einer Desktop-App erstellen kann.

## <a name="syntax"></a>Syntax


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppresentsite* \[ in\]
</dt> <dd>

Eine vorhandene Hostingschnittstelle. Weitere Informationen finden Sie unter **iviewobjectpresentnotifysite** in der Internet Explorer-Dokumentation.

</dd> <dt>

*pppresenter* \[ vorgenommen\]
</dt> <dd>

Die **\[ exclusiveto \]** -Schnittstelle für eine [**xamluipresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)-Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **HRESULT**-Standard, S ist für Erfolg **\_ OK** .

## <a name="remarks"></a>Bemerkungen

Zum Aufrufen dieser Methode ist eine **DllImport** -Windows.UI.Xaml.dll erforderlich.

Diese Methode kann nicht aus einer Windows Store-App aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows. UI. XAML-CoreTypes. idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Xamluipresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
