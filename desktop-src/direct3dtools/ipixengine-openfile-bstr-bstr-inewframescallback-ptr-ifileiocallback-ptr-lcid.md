---
description: Öffnet ein Grafikprotokoll.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine::OpenFile-Methode
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
ms.openlocfilehash: 8f6b2e34258221353baf541ddf76df205472f731
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624347"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile-Methode

Öffnet ein Grafikprotokoll.

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

*Dateiname*   
Eine COM-Zeichenfolge, die den Namen des Grafikprotokolls enthält.

*registryBoot*   
Eine COM-Zeichenfolge, die den Registrierungsstamm enthält. Die Engine sucht hier nach DIA und anderen Registrierungsschlüsseln.

*Rückrufe*   
Die Adresse einer Funktion, mit der der Host benachrichtigt wird, dass neue Frames analysiert wurden.

*pFileIOCallback*   
Die Adresse einer Funktion, mit der der Host während der Analyse über Datei-E/A-Fehler benachrichtigt wird.

*uiLocale*   
Die Gebietsschema-ID, die zum Anzeigen von Fehlermeldungen gemäß den Gebietsschemaeinstellungen verwendet wird.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
