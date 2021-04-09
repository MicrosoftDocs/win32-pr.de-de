---
description: Verwaltet die Konfiguration von Ressourcenpools mithilfe von Aufträgen.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862864"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a>CIM \_ resourcepoolconfigurationservice-Klasse

Verwaltet die Konfiguration von Ressourcenpools mithilfe von Aufträgen.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **CIM \_ resourcepoolconfigurationservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **CIM \_ resourcepoolconfigurationservice** -Klasse verfügt über diese Methoden.



| Methode                                                                                                          | BESCHREIBUNG                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Adresssourcestoresourcepool**](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | Startet einen Auftrag zum Hinzufügen von Ressourcen zu einem Ressourcenpool.<br/>                  |
| [**Changeparser-sourcepool**](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | Starten Sie einen Auftrag, um den übergeordneten Ressourcenpool eines Ressourcenpools zu ändern.<br/> |
| [**"Kreatechildresourcepool"**](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | Starten Sie einen Auftrag, um einen Ressourcenpool aus einem übergeordneten Ressourcenpool zu erstellen.<br/> |
| [**CreateResourcePool**](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | Startet einen Auftrag, um einen Stamm Ressourcenpool zu erstellen.<br/>                       |
| [**Deleteresourcepool**](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen.<br/>                             |
| [**Removeresourcesfromresourcepool**](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | Startet einen Auftrag, um Ressourcen aus einem Ressourcenpool zu entfernen.<br/>             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




