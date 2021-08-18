---
description: Die IProvidePropertyBuilder-Schnittstelle ermöglicht Objekten bei derEntität das Angeben von Eigenschaftengeneratorobjekten für Eigenschaften.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: IProvidePropertyBuilder-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: d6d82cdafbf775c7316ed882cf3776aaf216fcb82938825d8c939f21e60cc0e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750020"
---
# <a name="iprovidepropertybuilder-interface"></a>IProvidePropertyBuilder-Schnittstelle

Die **IProvidePropertyBuilder-Schnittstelle** ermöglicht Objekten bei derEntität das Angeben von Eigenschaftengeneratorobjekten für Eigenschaften. Generatoren werden über eine Schaltfläche mit Auslassungsauslassung ( ... ) im Microsoft Visual Studio-Eigenschaftenbrowser aufgerufen und über \[ \] [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) aufgerufen, wenn die Schaltfläche gedrückt wird. Um einen Generator für eine bestimmte Eigenschaft zu erstellen, geben Sie eine GUID für den Eigenschaften-Generator zurück, die für die aktuelle Eigenschaft von [**MapPropertyToBuilder aufgerufen werden soll.**](iprovidepropertybuilder-mappropertytobuilder.md) Generatoren werden in der Regel über modale Dialogfelder implementiert.

Die Version für diese Schnittstelle ist 1.0. Methodenaufrufe werden an einem dynamisch zugewiesenen Endpunkt empfangen (wie in der binären MSMQ-Dokumentation zur Endpunktzuordnung beschrieben) und verwenden die UUID (universell eindeutiger Bezeichner) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".

## <a name="members"></a>Member

Die **IProvidePropertyBuilder:IUnknown-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IProvidePropertyBuilder** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IProvidePropertyBuilder:IUnknown-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                       | Beschreibung                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | Benachrichtigt ein Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
