---
description: Die VerifyDiskSpace-Eigenschaft ist eine schreibgeschützte Eigenschaft.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Session.VerifyDiskSpace-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4a50bb96088f2c52673fda9a9ddffd786657376bcb4e4a60d5c6d81cb4fbe5e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628760"
---
# <a name="sessionverifydiskspace-property"></a>Session.VerifyDiskSpace-Eigenschaft

Die **VerifyDiskSpace-Eigenschaft** ist eine schreibgeschützte Eigenschaft. Sie gibt TRUE zurück, wenn genügend Speicherplatz vorhanden ist, und FALSE, wenn der Datenträger voll ist. Da diese Eigenschaft von den Kostenkostenaktionen gesammelte Informationen verwendet, sollte **VerifyDiskSpace** nur nach der [Aktion CostInitialize,](costinitialize-action.md)der [FileCost-Aktion](filecost-action.md)und [der CostFinalize-Aktion](costfinalize-action.md)aufgerufen werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



 

 




