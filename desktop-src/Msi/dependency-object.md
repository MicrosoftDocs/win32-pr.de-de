---
description: Das Dependency-Objekt gibt ein Modul zurück, von dem das aktuelle Modul abhängig ist und das noch nicht mit der aktuellen Installationsdatenbank zusammengeführt wurde.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Abhängigkeitsobjekt (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: ac5786dcf3d4818fdfb3f0458cbfa85c923e5200ae69b5cb93d38330c322abf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378889"
---
# <a name="dependency-object"></a>Abhängigkeitsobjekt

Das **Dependency-Objekt** gibt ein Modul zurück, von dem das aktuelle Modul abhängig ist und das noch nicht mit der aktuellen Installationsdatenbank zusammengeführt wurde.

## <a name="members"></a>Member

Das **Dependency-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Abhängigkeitsobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Sprache**](dependency-language.md)<br/> | Gibt die Sprache des Moduls zurück.<br/>           |
| [**Modul**](dependency-module.md)<br/>     | Gibt die Modul-ID des erforderlichen Moduls zurück.<br/> |
| [**Version**](dependency-version.md)<br/>   | Gibt die Version des erforderlichen Moduls zurück.<br/>   |



 

## <a name="c"></a>C++

**schnittstelle IMsmDependency : IDispatch**

## <a name="interface-id"></a>Schnittstellen-ID



| Konstante                | Wert                                  |
|-------------------------|----------------------------------------|
| **\_IID-IMsmDependency** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




