---
description: Die iprovidebug PropertyBuilder-Schnittstelle ermöglicht es Objekten, Eigenschafts Generator Objekte für Eigenschaften anzugeben, wenn Sie implementiert wird.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Iprovidebug PropertyBuilder-Schnittstelle
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
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357548"
---
# <a name="iprovidepropertybuilder-interface"></a>Iprovidebug PropertyBuilder-Schnittstelle

Die **iprovidebug PropertyBuilder** -Schnittstelle ermöglicht es Objekten, Eigenschafts Generator Objekte für Eigenschaften anzugeben, wenn Sie implementiert wird. Generatoren werden durch eine Schaltfläche mit Auslassungs Zeichen ( \[ ... \] ) im Microsoft Visual Studio Eigenschaften Browser aufgerufen und durch [**executebuilder**](iprovidepropertybuilder-executebuilder.md) aufgerufen, wenn die Schaltfläche gedrückt wird. Wenn Sie einen Generator für eine bestimmte Eigenschaft bereitstellen möchten, geben Sie eine GUID für den Eigenschaften-Generator zurück, die für die aktuelle Eigenschaft von [**mappropertytobuilder**](iprovidepropertybuilder-mappropertytobuilder.md)aufgerufen werden soll. Generatoren werden in der Regel über modale Dialogfelder implementiert.

Die Version für diese Schnittstelle ist 1,0. Methodenaufrufe werden an einem dynamisch zugewiesenen Endpunkt empfangen (wie in der MSMQ-Binär Dokumentation zur Endpunkt Zuordnung beschrieben) und verwenden die UUID (universell eindeutiger Bezeichner) "33c0c1d8-33cf-11d3-bff2-00c04f990235".

## <a name="members"></a>Member

Die **iprovidäpropertybuilder: IUnknown** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iproviabpropertybuilder** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iprovidepropertybuilder: IUnknown** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Executebuilder**](iprovidepropertybuilder-executebuilder.md)             | Benachrichtigt ein-Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.<br/> |
| [**Mappropertytbuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
