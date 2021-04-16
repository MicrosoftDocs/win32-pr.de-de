---
title: Die Methode "ltactiveserver" der Win32_RDMSEnvironment-Klasse
description: Legt den FQDN der RDMs-Umgebung (Remotedesktop Management Services) auf den aktuellen Knoten fest.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Klasse "Win32_RDMSEnvironment"
- Win32_RDMSEnvironment Klasse Remotedesktopdienste, Methode "Methode"
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476419"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Die Methode "ltactiveserver" der Win32- \_ Klasse "rdmsenvironment"

Legt den FQDN der RDMs-Umgebung (Remotedesktop Management Services) auf den aktuellen Knoten fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdmsenvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





