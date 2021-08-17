---
description: Beendet die Auslösung und schließt das Grafikprotokoll ab.
MS-HAID: vspixengine.IPixEngine2\_EndExperiment\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2::EndExperiment-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0260F337-B279-4FE6-92F3-FCF70C2B8980
api_name:
- IPixEngine2.EndExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 72c3893e3cadff355fd3d082b119a3a86d483c706265f66b90a26e56b371bc2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456950"
---
# <a name="span-idvspixengineipixengine2_endexperiment_bstr_ifileiocallback_ptrspanipixengine2endexperiment-method"></a><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>IPixEngine2::EndExperiment-Methode

Beendet die Auslösung und schließt das Grafikprotokoll ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndExperiment(
   BSTR              logFile,
   IFileIOCallback * pCallback
);
```

## <a name="parameters"></a>Parameter

*Logfile*   
Eine COM-Zeichenfolge, die den Namen des Grafikprotokolls enthält.

*pCallback*   
Die Adresse eines Rückrufs, der verwendet wird, um anzugeben, dass die Auslösung beendet wurde.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
