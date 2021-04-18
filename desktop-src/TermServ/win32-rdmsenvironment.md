---
title: Win32_RDMSEnvironment-Klasse
description: Verwaltet eine RDMs-Umgebung (Remotedesktop Management Services).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste
- Win32_RDMSEnvironment Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339560"
---
# <a name="win32_rdmsenvironment-class"></a>Win32 \_ rdmsenvironment-Klasse

Verwaltet eine RDMs-Umgebung (Remotedesktop Management Services).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsenvironment** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdmsenvironment** -Klasse verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Getactiveserver**](getactiveserver-win32-rdmsenvironment.md)         | Ruft den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) der RDMs-Umgebung ab.<br/>                 |
| [**Getclientaccessname**](getclientaccessname-win32-rdmsenvironment.md) | Ruft den Namen der RDMs-Umgebung des Domain Name System (DNS)-Ressourceneinsatzes (RR) ab.<br/> |
| [**"Abtactiveserver"**](setactiveserver-win32-rdmsenvironment.md)         | Legt den FQDN der RDMs-Umgebung auf den aktuellen Knoten fest.<br/>                                |
| [**Setclientaccessname**](setclientaccessname-win32-rdmsenvironment.md) | Aktualisiert den DNS-RR-Namen der RDMs-Umgebung.<br/>                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

 





