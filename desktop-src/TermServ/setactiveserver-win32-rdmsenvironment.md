---
title: SetActiveServer-Methode der Win32_RDMSEnvironment-Klasse
description: Legt den FQDN der RDMS-Umgebung (Remotedesktop Management Services) auf den aktuellen Knoten fest.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- SetActiveServer-Methode Remotedesktopdienste
- SetActiveServer-Methode Remotedesktopdienste , Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment Klasse Remotedesktopdienste , SetActiveServer-Methode
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
ms.openlocfilehash: b68a8f9c6661e78932893ef25278234fb4c944d22297cb87cc95aebe9bc8d8ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865490"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a>SetActiveServer-Methode der Win32 \_ RDMSEnvironment-Klasse

Legt den FQDN der RDMS-Umgebung (Remotedesktop Management Services) auf den aktuellen Knoten fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSUmgebung**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





