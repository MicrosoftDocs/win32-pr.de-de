---
title: MCI_MSF_SECOND-Makro (mciapi. h)
description: Das MCI \_ MSF \_ Second-Makro ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen über die gepackten Minuten/Sekunden/Frames (MSF) enthält
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858984"
---
# <a name="mci_msf_second-macro"></a>MCI \_ MSF- \_ zweites Makro

Das **MCI \_ MSF \_ Second** -Makro ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen über die gepackten Minuten/Sekunden/Frames (MSF) enthält

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwmsf* 
</dt> <dd>

Uhrzeit im MSF-Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Sekunden Komponente der angegebenen MSF-Informationen zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im MSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Minuten enthält, dem nächst bedeutsamen Byte, das Sekunden enthält, und dem nächstniedrigsten Byte mit Frames ausgedrückt. Das signifikanteste Byte wird nicht verwendet.

Das **MCI \_ MSF \_ Second** -Makro wird wie folgt definiert:


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Makros](mci-macros.md)
</dt> </dl>

 

 





