---
description: Verwaltet die Sammlungen auf dem Hyper-V-Host.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760495"
---
# <a name="msvm_collectionmanagementservice-class"></a>MSVM \_ collectionmanagementservice-Klasse

Verwaltet die Sammlungen auf dem Hyper-V-Host.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **MSVM \_ collectionmanagementservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM \_ collectionmanagementservice** -Klasse verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddMember**](msvm-collectionmanagementservice-addmember.md)                 | Fügt das angegebene managedelta-Element als Member des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts hinzu.<br/>                                                                                           |
| [**Definecollection**](msvm-collectionmanagementservice-definecollection.md)   | Erstellt ein neues [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt.<br/>                                                                                                                                        |
| [**Destroycollection**](msvm-collectionmanagementservice-destroycollection.md) | Löscht das angegebene [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt.<br/>                                                                                                                                    |
| [**RemoveMember**](msvm-collectionmanagementservice-removemember.md)           | Entfernt das angegebene managedelta-Element als Member des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts.<br/>                                                                                        |
| [**Removemitgliedbyid**](msvm-collectionmanagementservice-removememberbyid.md)   | Entfernt das angegebene managedelta-Element als Member der [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) mit dem angegebenen Bezeichner. Dies ist auch dann erfolgreich, wenn das Objekt mit diesem Bezeichner nicht vorhanden ist.<br/> |
| [**Renamecollection**](msvm-collectionmanagementservice-renamecollection.md)   | Aktualisiert den Elementname des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts.<br/>                                                                                                                    |
| [**Start Service**](msvm-collectionmanagementservice-startservice.md)           | Startet den Dienst.<br/>                                                                                                                                                                                                |
| [**Stop Service**](msvm-collectionmanagementservice-stopservice.md)             | Beendet den Dienst.<br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




