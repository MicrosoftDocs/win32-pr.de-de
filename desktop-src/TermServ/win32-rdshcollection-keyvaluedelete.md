---
title: Keyvaluedelete-Methode der Win32_RDSHCollection-Klasse
description: Löscht den angegebenen Schlüssel (und zugeordneten Wert) aus der Auflistung.
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- Keyvaluedelete-Methode Remotedesktopdienste
- Keyvaluedelete-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, keyvaluedelete-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949737"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a>Keyvaluedelete-Methode der Win32 \_ rdshcollection-Klasse

Löscht den angegebenen Schlüssel (und zugeordneten Wert) aus der Auflistung.

## <a name="syntax"></a>Syntax


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der zu löschende Schlüssel.

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

 

 





