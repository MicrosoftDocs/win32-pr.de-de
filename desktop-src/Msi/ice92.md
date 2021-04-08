---
description: ICE92 überprüft, ob eine Komponente ohne Komponenten-ID-GUID nicht auch als permanente Komponente angegeben wird.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866088"
---
# <a name="ice92"></a>ICE92

ICE92 überprüft, ob eine Komponente ohne Komponenten-ID-GUID nicht auch als permanente Komponente angegeben wird. Diese benutzerdefinierte Ice-Aktion überprüft die Komponenten [Tabelle](component-table.md) auf Komponenten, die keine [GUID](guid.md) im Feld "ComponentId" aufweisen, und überprüft, ob das **msidbcomponentattributespermanent** -Flag im Feld "Attribute" nicht festgelegt wurde. ICE92 überprüft auch, ob keine Komponente sowohl das **msidbcomponentattributespermanent** -Attribut als auch das **msidbcomponentattributesuninstallonabgelöst** -Attribut aufweist.

Wenn die ComponentID-Spalte NULL ist, registriert das Installationsprogramm die Komponente nicht, und die Komponente kann vom Installationsprogramm nicht entfernt oder repariert werden.

## <a name="result"></a>Ergebnis

ICE92 gibt den folgenden Fehler aus.



| ICE92-Fehler                                                          | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Komponente ' \[ 1 \] ' weist keine ComponentID auf und ist als permanent gekennzeichnet. | Der Eintrag für diese Komponente in der Component-Tabelle weist in der ComponentID-Spalte den Wert NULL auf und weist **msidbcomponentattributespermanent** in der Spalte Attribute auf. |



 

ICE92 gibt die folgende Warnung aus.



| ICE92-Warnung                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Komponente " \[ 1 \] " ist als permanent gekennzeichnet und wird bei der Deinstallation deinstalliert. Das Uninstall-on-Ablösung-Attribut wird ignoriert, da die Komponente permanent ist. | Der Eintrag für diese Komponente in der [Komponenten Tabelle](component-table.md) enthält sowohl das **msidbcomponentattributespermanente** -Attribut als auch das **msidbcomponentattributesuninstallonabgelöst** -Attribut. |



 

## <a name="example"></a>Beispiel

ICE92 meldet den folgenden Fehler für das Beispiel:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | ComponentID | Verzeichnis\_ | Attribute | KEYPATH |
|------------|-------------|-------------|------------|---------|
| Component1 |             | Directoren  | 16         | Mit der   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



