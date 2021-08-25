---
description: ICEM11 überprüft, ob ein konfigurierbares Mergemodul die ModuleConfiguration-Tabelle und die ModuleSubsators-Tabelle in der ModuleIgnoreTable-Tabelle des Moduls auflistet.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157248d62f43a0b1a791220e2aeb917ba8273d31b93de69078f9876cddbd2748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894430"
---
# <a name="icem11"></a>ICEM11

ICEM11 überprüft, ob ein konfigurierbares Mergemodul die [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) und die [ModuleSubsators-Tabelle](modulesubstitution-table.md) in der [ModuleIgnoreTable-Tabelle](moduleignoretable-table.md) des Moduls auflistet. Dadurch wird sichergestellt, dass Mergetools, die konfigurierbare Mergemodule (weniger als Version 2.0) nicht erkennen, diese Tabellen nicht in die Zieldatenbank kopieren.

Dieses ICEM ist in der Datei Mergemod.cub verfügbar, die im Windows Installer 2.0 SDK und höher bereitgestellt wird. Weitere Informationen finden Sie [unter Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Ergebnis

ICEM11 gibt einen Fehler aus, wenn das Modul eine ModuleConfiguration- oder ModuleSubsisierungstabelle enthält, die nicht in der Tabelle ModuleIgnoreTable aufgeführt ist.

## <a name="example"></a>Beispiel

ICEM11 stellt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen zur Verfügung.

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[ModuleConfiguration](moduleconfiguration-table.md) (partiell)



| Name     | Format | type   | ContextData | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Binary | Symbol        | DefaultIcon  |



 

[ModuleSubsmodul](modulesubstitution-table.md)



| Tabelle   | Zeile              | Spalte | Wert        |
|---------|------------------|--------|--------------|
| Control | Dialog1; Control1 | Text   | \[IconKey1\] |



 

[ModuleIgnoreTable](moduleignoretable-table.md)



| Tabelle               |
|---------------------|
| ModuleConfiguration |



 

Um diesen Fehler zu beheben, schließen Sie die Tabellen ModuleSubs sowie ModuleConfiguration in die Tabelle ModuleIgnoreTable ein.

## <a name="table-used-during-execution"></a>Während der Ausführung verwendete Tabelle

[ModuleSubsmodul](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[ModuleIgnoreTable](moduleignoretable-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Merge Module ICE Reference](merge-module-ice-reference.md)
</dt> </dl>

 

 



