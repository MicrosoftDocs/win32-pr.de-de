---
description: Beschreibt einen Referenzpunkt Dienst für virtuelle Systeme.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357149"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a>MSVM \_ virtualsystemreferencepointservice-Klasse

Beschreibt einen Referenzpunkt Dienst für virtuelle Systeme.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemreferencepointservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM \_ virtualsystemreferencepointservice** -Klasse verfügt über diese Methoden.



| Methode                                                                                                       | BESCHREIBUNG                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**"Kreatereferencepoint"**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | Erstellt einen Referenzpunkt eines virtuellen Systems.<br/>            |
| [**Destroyreferencepoint**](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | Löscht den angegebenen Verweis Punkt.<br/>                    |
| [**Exportreferencepoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | Exportiert den Verweis Punkt des virtuellen Systems.<br/>        |
| [**Importreferencepointmetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | Importiert Verweis Punkt Metadaten des virtuellen Systems.<br/>   |
| [**Removeassociateddata**](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.<br/> |



 

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

 

 




