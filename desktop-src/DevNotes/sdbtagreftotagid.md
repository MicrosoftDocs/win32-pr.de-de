---
description: Ruft die TagID und ein Handle für die Shimdatenbank für die angegebene tagref ab.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: Sdbtagrebtotagid-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126386"
---
# <a name="sdbtagreftotagid-function"></a>Sdbtagrebtotagid-Funktion

Ruft die **TagID** und ein Handle für die Shimdatenbank für die angegebene [**tagref**](tagref.md)ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsdb* \[ in\]
</dt> <dd>

Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.

</dd> <dt>

*trwem* \[ in\]
</dt> <dd>

Die [**tagref**](tagref.md).

</dd> <dt>

*ppdb* \[ vorgenommen\]
</dt> <dd>

Das resultierende Handle der Shimdatenbank.

</dd> <dt>

*ptiwhat* \[ vorgenommen\]
</dt> <dd>

Die resultierende **TagID**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbinitdatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TagID**](tagid.md)
</dt> <dt>

[**Tagref**](tagref.md)
</dt> </dl>

 

 




