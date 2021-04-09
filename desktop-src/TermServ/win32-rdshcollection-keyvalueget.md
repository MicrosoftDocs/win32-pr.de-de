---
title: Keyvalueget-Methode der Win32_RDSHCollection-Klasse
description: Ruft den Wert ab, der dem angegebenen Schlüssel in der Auflistung zugeordnet ist.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Keyvalueget-Methode Remotedesktopdienste
- Keyvalueget-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, keyvalueget-Methode
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
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858804"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>Keyvalueget-Methode der Win32 \_ rdshcollection-Klasse

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

*Schlüssel* \[ in\]
</dt> <dd>

Der Schlüssel, der den Wert identifiziert, den Sie abrufen möchten.

</dd> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg wird der Wert zurückgegeben, der dem angegebenen Schlüssel zugeordnet ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdshcollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





