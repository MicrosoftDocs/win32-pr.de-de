---
description: Dienst zum Erstellen, zerstören und Exportieren von Bezugspunkten.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347004"
---
# <a name="msvm_collectionreferencepointservice-class"></a>MSVM \_ collectionreferencepointservice-Klasse

Dienst zum Erstellen, zerstören und Exportieren von Bezugspunkten

von virtuellen System Sammlungen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **MSVM \_ collectionreferencepointservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM \_ collectionreferencepointservice** -Klasse verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatereferencepoint"**](msvm-collectionreferencepointservice-createreferencepoint.md)   | Erstellt einen Referenzpunkt einer Sammlung virtueller Systeme.<br/>                                                                                                                                            |
| [**Destroyreferencepoint**](msvm-collectionreferencepointservice-destroyreferencepoint.md) | Zerstört eine vorhandene Verweis Punkt Auflistung. Diese Methode kann als Nebeneffekt andere Verweis Punkte zerstören, die von der betroffenen Verweis Punkt Auflistung abhängig sind.<br/>                      |
| [**Exportreferencepoint**](msvm-collectionreferencepointservice-exportreferencepoint.md)   | Exportiert eine Verweis Punkt Auflistung in eine Datei. In der resultierenden Datei werden die Verweis Punkt Auflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen beibehalten.<br/> |
| [**Removeassociateddata**](msvm-collectionreferencepointservice-removeassociateddata.md)   | Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.<br/>                                                                                                                                            |



 

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

 

 




