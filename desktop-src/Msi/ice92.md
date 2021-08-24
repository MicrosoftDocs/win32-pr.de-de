---
description: ICE92 überprüft, ob eine Komponente ohne Komponenten-ID-GUID nicht auch als permanente Komponente angegeben ist.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd96126f9255303bb2d78f39bc6fef4312859533d1298b9a9d30afd1b79575fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894880"
---
# <a name="ice92"></a>ICE92

ICE92 überprüft, ob eine Komponente ohne Komponenten-ID-GUID nicht auch als permanente Komponente angegeben ist. Diese benutzerdefinierte ICE-Aktion überprüft die [Komponententabelle](component-table.md) auf Komponenten ohne [guid,](guid.md) die im Feld ComponentId angegeben ist, und überprüft, ob das **Flag msidbComponentAttributesPermanent** nicht im Feld Attribute festgelegt wurde. ICE92 überprüft auch, ob keine Komponente über die Attribute **msidbComponentAttributesPermanent** und **msidbComponentAttributesUninstallOnSupersedence verfügt.**

Wenn die ComponentId-Spalte NULL ist, registriert das Installationsprogramm die Komponente nicht, und die Komponente kann nicht vom Installationsprogramm entfernt oder repariert werden.

## <a name="result"></a>Ergebnis

ICE92 gibt den folgenden Fehler aus.



| ICE92-Fehler                                                          | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Komponente \[ "1" \] hat keine ComponentId und ist als permanent markiert. | Der Eintrag für diese Komponente in der Component-Tabelle weist null in der ComponentId -Spalte und **msidbComponentAttributesPermanent** in der Attributes -Spalte auf. |



 

ICE92 gibt die folgende Warnung aus.



| ICE92-Warnung                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Komponente \[ "1" \] ist als permanent markiert, und die Deinstallation erfolgt bei Ablösung. Das Attribut uninstall-on-supersedence wird ignoriert, da die Komponente dauerhaft ist. | Für den Eintrag für diese Komponente in der [Component-Tabelle](component-table.md) sind sowohl die Attribute **msidbComponentAttributesPermanent** als auch **msidbComponentAttributesUninstallOnSupersedence** angegeben. |



 

## <a name="example"></a>Beispiel

ICE92 meldet den folgenden Fehler für das Beispiel:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Komponententabelle](component-table.md) (teilweise)



| Komponente  | Componentid | Verzeichnis\_ | Attribute | KeyPath |
|------------|-------------|-------------|------------|---------|
| Komponente1 |             | DirectoryA  | 16         | Filea   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



