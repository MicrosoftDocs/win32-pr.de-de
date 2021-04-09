---
title: Freerootkauseinfos-Funktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von rootkauseingefo-Strukturen auf.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- Freerootcauseingefos-Funktion NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740896"
---
# <a name="freerootcauseinfos-function"></a>Freerootkausan Fos-Funktion

Die **freerootkausan Fos** -Funktion hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von [**rootkauseingefo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) -Strukturen auf. Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.

## <a name="syntax"></a>Syntax


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* \[ in\]
</dt> <dd>

Typ: **[**rootkauseinfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Das Array von-Strukturen. Der zugewiesene Speicher, auf den diese Strukturen zeigen, wird freigegeben.

</dd> <dt>

_RootCauseCount * 
</dt> <dd>

Typ: **ulong**

Die Anzahl der Strukturen im Array, auf die von *pinfo* verwiesen wird.

</dd> <dt>

*bfrepointer* 
</dt> <dd>

Typ: **bool**

True, wenn das Array von-Strukturen ebenfalls gelöscht werden soll. andernfalls false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rootkauseingefo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

