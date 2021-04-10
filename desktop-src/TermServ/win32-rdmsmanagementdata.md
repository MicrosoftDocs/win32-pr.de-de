---
title: Win32_RDMSManagementData-Klasse
description: Synchronisiert Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Win32_RDMSManagementData-Klasse Remotedesktopdienste
- Win32_RDMSManagementData Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040200"
---
# <a name="win32_rdmsmanagementdata-class"></a>Win32 \_ rdmsmanagementdata-Klasse

Synchronisiert Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsmanagementdata** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdmsmanagementdata** -Klasse verfügt über diese Methoden.



| Methode                                                                                        | BESCHREIBUNG                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Synchronizeallpublishingdata**](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | Synchronisiert alle Veröffentlichungsdaten für RDMs.<br/>                  |
| [**Synchronizepublishingdata**](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | Synchronisiert den angegebenen Satz von Veröffentlichungsdaten für RDMs.<br/> |



 

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

 

 





