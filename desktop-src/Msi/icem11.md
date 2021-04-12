---
description: ICEM11 überprüft, ob ein konfigurierbares Mergemodul die ModuleConfiguration-Tabelle und die ModuleSubstitution-Tabelle in der moduleignoretable-Tabelle des Moduls auflistet.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216940"
---
# <a name="icem11"></a>ICEM11

ICEM11 überprüft, ob ein konfigurierbares Mergemodul die [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) und die [ModuleSubstitution](modulesubstitution-table.md) -Tabelle in der [moduleignoretable-Tabelle](moduleignoretable-table.md) des Moduls auflistet. Dadurch wird sichergestellt, dass Merge-Tools, die konfigurierbare Mergemodule nicht erkennen (weniger als Version 2,0) diese Tabellen nicht in die Zieldatenbank kopieren.

Dieses ICEM ist in der Datei "Mergemod. Cub" verfügbar, die im SDK für Windows Installer 2,0 und höher bereitgestellt wird. Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Ergebnis

ICEM11 gibt einen Fehler aus, wenn das Modul eine ModuleConfiguration-oder ModuleSubstitution-Tabelle enthält, die nicht in der moduleignoretable-Tabelle aufgeführt ist.

## <a name="example"></a>Beispiel

ICEM11 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[ModuleConfiguration](moduleconfiguration-table.md) (partiell)



| Name     | Format | type   | ContextData | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Binary | Symbol        | DefaultIcon  |



 

[ModuleSubstitution](modulesubstitution-table.md)



| Tabelle   | Zeile              | Spalte | Wert        |
|---------|------------------|--------|--------------|
| Control | Dialog1; Control1 | Text   | \[IconKey1\] |



 

[Moduleignoretable](moduleignoretable-table.md)



| Tabelle               |
|---------------------|
| ModuleConfiguration |



 

Um diesen Fehler zu beheben, schließen Sie die Tabellen ModuleSubstitution und ModuleConfiguration in der Tabelle moduleignoretable ein.

## <a name="table-used-during-execution"></a>Während der Ausführung verwendete Tabelle

[ModuleSubstitution](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[Moduleignoretable](moduleignoretable-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



