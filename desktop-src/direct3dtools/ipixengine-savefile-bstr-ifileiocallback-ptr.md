---
description: Speichert das Grafikprotokoll am angegebenen Speicherort.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine::SaveFile-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 737a0de1636fbae4f8beee0be89780b54415e138
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622536"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile-Methode

Speichert das Grafikprotokoll am angegebenen Speicherort.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a>Parameter

*Dateiname*   
Eine COM-Zeichenfolge, die den Pfadnamen des gespeicherten Grafikprotokolls enthält.

*pFileIOCallback*   
Die Adresse eines Functons, der verwendet wird, um den Host während des Speicherns über Datei-E/A-Fehler zu benachrichtigen.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
