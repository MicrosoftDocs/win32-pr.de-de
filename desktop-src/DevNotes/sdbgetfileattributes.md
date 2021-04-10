---
description: Ruft die Attributdaten für die angegebene Datei ab.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Sdbgetfileattribute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125624"
---
# <a name="sdbgetfileattributes-function"></a>Sdbgetfileattribute-Funktion

Ruft die Attributdaten für die angegebene Datei ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpwszfilename* \[ in\]
</dt> <dd>

Der Pfad zur Datei.

</dd> <dt>

*ppattrinfo* \[ vorgenommen\]
</dt> <dd>

Ein Array von [**attrinfo**](attrinfo.md) -Strukturen, die die Attributdaten enthalten.

</dd> <dt>

*lpdwattrcount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Attribute.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie mit den Daten fertig sind, können Sie Sie mit der [**sdbfreefileattribute**](sdbfreefileattributes.md) -Funktion freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbformatattribute**](sdbformatattribute.md)
</dt> <dt>

[**Sdbfrefileattribute**](sdbfreefileattributes.md)
</dt> </dl>

 

 




