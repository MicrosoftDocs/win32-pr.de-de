---
title: KeyValueGet-Methode der Win32_RDSHCollection Klasse
description: Ruft den Wert ab, der dem angegebenen Schlüssel in der Auflistung zugeordnet ist.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- KeyValueGet-Remotedesktopdienste
- KeyValueGet-Methode Remotedesktopdienste , Win32_RDSHCollection-Klasse
- Win32_RDSHCollection klasse Remotedesktopdienste , KeyValueGet-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 943db8db044758e7f78e7d79b4ae5280c6ce51281b5858237a24e5f83add33a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422680"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>KeyValueGet-Methode der Win32 \_ RDSHCollection-Klasse

Ruft den Wert ab, der dem angegebenen Schlüssel in der Auflistung zugeordnet ist.

## <a name="syntax"></a>Syntax


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Der Schlüssel, der den Wert identifiziert, den Sie abrufen möchten.

</dd> <dt>

*Wert* \[ out\]
</dt> <dd>

Bei Erfolg gibt den Wert zurück, der dem angegebenen Schlüssel zugeordnet ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





