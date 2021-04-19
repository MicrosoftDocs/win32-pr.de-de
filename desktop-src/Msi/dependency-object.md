---
description: Das Abhängigkeits Objekt gibt ein Modul zurück, von dem das aktuelle Modul abhängig ist und das noch nicht mit der aktuellen Installations Datenbank zusammengeführt wurde.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Abhängigkeits Objekt (Mergemod. h)
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
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359399"
---
# <a name="dependency-object"></a>Abhängigkeitsobjekt

Das **Abhängigkeits** Objekt gibt ein Modul zurück, von dem das aktuelle Modul abhängig ist und das noch nicht mit der aktuellen Installations Datenbank zusammengeführt wurde.

## <a name="members"></a>Member

Das **Abhängigkeits** Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Abhängigkeits** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Sprache**](dependency-language.md)<br/> | Gibt die Sprache des Moduls zurück.<br/>           |
| [**Modul**](dependency-module.md)<br/>     | Gibt die Modul-ID des erforderlichen Moduls zurück.<br/> |
| [**Version**](dependency-version.md)<br/>   | Gibt die Version des erforderlichen Moduls zurück.<br/>   |



 

## <a name="c"></a>C++

Schnittstelle **imsmdependenz: IDispatch**

## <a name="interface-id"></a>Schnittstellen-ID



| Konstante                | Wert                                  |
|-------------------------|----------------------------------------|
| **IID \_ imsmabhängigkeit** | {0adda82d-2c26-11d2-Ad65-00a0c9af11a6} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




