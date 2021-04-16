---
description: Speichert das Grafik Protokoll an der angegebenen Position.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixengine:: SaveFile-Methode'
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
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522723"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>Ipixengine:: SaveFile-Methode

Speichert das Grafik Protokoll an der angegebenen Position.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a>Parameter

*Einfügen*   
Eine com-Zeichenfolge, die den Pfadnamen des gespeicherten Grafik Protokolls enthält.

*pfileiocallback*   
Die Adresse eines funktons, mit dem der Host von Datei-e/a-Fehlern beim Speichern benachrichtigt wird

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipixengine**](/windows/desktop/direct3dtools/ipixengine)

 

 
