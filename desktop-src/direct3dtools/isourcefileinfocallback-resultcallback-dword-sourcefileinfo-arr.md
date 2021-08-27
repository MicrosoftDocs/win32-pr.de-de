---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Informationen zu Quelldateien zu informieren, die der Aufrufstapel zugeordnet sind.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISourceFileInfoCallback::ResultCallback-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a50dba592f67a4628501d6a9a92bfe379daed09
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626346"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über Informationen zu Quelldateien zu informieren, die der Aufrufstapel zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a>Parameter

*Count*   
Die Anzahl der zurückgegebenen Quelldateien.

*count0 \_ sourceFileInfoBuffer*   
Die Quelldateien.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**ISourceFileInfoCallback**](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
