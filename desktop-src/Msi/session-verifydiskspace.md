---
description: Die verifydiskspace-Eigenschaft ist eine schreibgeschützte Eigenschaft.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Session. verifydiskspace-Eigenschaft
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
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356087"
---
# <a name="sessionverifydiskspace-property"></a>Session. verifydiskspace-Eigenschaft

Die **verifydiskspace** -Eigenschaft ist eine schreibgeschützte Eigenschaft. Sie gibt true zurück, wenn ausreichend Speicherplatz vorhanden ist, und false, wenn der Datenträger voll ist. Da diese Eigenschaft Informationen verwendet, die von den Kosten Aktionen gesammelt werden, sollte **verifydiskspace** nur nach der Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" aufgerufen werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




