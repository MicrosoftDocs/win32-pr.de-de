---
description: Öffnet ein Grafik Protokoll.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixengine:: OpenFile-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124339"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Ipixengine:: OpenFile-Methode

Öffnet ein Grafik Protokoll.

## <a name="syntax"></a>Syntax


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a>Parameter

*Einfügen*   
Eine com-Zeichenfolge, die den Namen des Grafik Protokolls enthält.

*registryboot*   
Eine com-Zeichenfolge, die den Registrierungs Stamm enthält. Die Engine sucht hier nach Dia und anderen Registrierungs Schlüsseln.

*Rückrufe*   
Die Adresse einer Funktion, die verwendet wird, um den Host zu benachrichtigen, dass neue Frames analysiert wurden.

*pfileiocallback*   
Die Adresse einer Funktion, die verwendet wird, um den Host von Datei-e/a-Fehlern beim Parsen zu Benachrichtigen

*uilocale*   
Die Gebiets Schema-ID, die zum Darstellen von Fehlermeldungen gemäß Gebiets Schema Einstellungen verwendet wird.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipixengine**](/windows/desktop/direct3dtools/ipixengine)

 

 
