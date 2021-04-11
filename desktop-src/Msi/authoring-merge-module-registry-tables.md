---
description: Verwenden Sie die Merge Module-Registrierungs Tabellen gemäß dem Typ der Registrierungsinformationen.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Erstellen von Mergemodul-Registrierungs Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959515"
---
# <a name="authoring-merge-module-registry-tables"></a>Erstellen von Mergemodul-Registrierungs Tabellen

Verwenden Sie die Merge Module-Registrierungs Tabellen gemäß dem Typ der Registrierungsinformationen.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>TypeLib, Class, AppID, ProgID, Extension, Verb oder MIME-Tabellen

Für Typbibliotheken, Klassen, Erweiterungen und Verben erstellen Sie Registrierungsinformationen in den Tabellen [typelib](typelib-table.md), [Klasse](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)oder [MIME](mime-table.md) des Mergemoduls. Wenn Sie die [Registrierungs Tabelle](registry-table.md) zum Hinzufügen dieser Informationen verwenden, kann Windows 2000 keine systemweiten Ankündigungen für diese Komponenten bereitstellen.

Autoren von Mergemodulen können sich aus den folgenden Gründen entscheiden, sich nicht mithilfe der Klassen Tabelle zu registrieren:

-   Um von der Klassen Tabelle registriert zu werden, muss es sich bei der Datei um den KEYPATH der zugehörigen Komponente handeln. Dies erfordert möglicherweise eine akzeptable Änderung in der Organisation der Komponenten.
-   Ein com-Befehl löst möglicherweise einen Installationsversuch aus, eine angekündigte Klasse erneut zu installieren. Autoren können sich entscheiden, eine Klasse nicht mithilfe der Klassen Tabelle zu registrieren, um zu vermeiden, dass eine Neuinstallation ausgelöst wird, wenn der Client Computer eine Benutzeroberfläche nicht unterstützt.

## <a name="registry-table"></a>Registrierungs Tabelle

Verwenden Sie die Registrierungs Tabelle, um Registrierungsinformationen hinzuzufügen, die nicht in den Tabellen TypeLib, Klasse, AppID, ProgID, Extension, Verb oder MIME erstellt werden können. Windows 2000 kann keine systemweite Ankündigung für Komponenten bereitstellen, die die Registrierungs Tabelle verwenden.

Wenn Sie die Registrierungs Tabelle erstellen, finden Sie weitere Informationen unter Dateipfade mithilfe der \[ \# Datei \] \[ . Datei \] Format anstelle von \[ Verzeichnis \] Dateiname. Das letztere Format unterstützt keine Installation von "Run-From-Source". Im ersten Format werden fehlende Dateien und fehlerhafte Komponenten leichter erkannt.

Bei der Verwendung von formatiertem Text in der Schlüssel Spalte der Registrierungs Tabelle ist Vorsicht geboten. Da Windows Installer keine Komponenten neu installiert, die bereits installiert sind, kann die Verwendung von formatiertem Text in diesem Feld dazu führen, dass Registrierungsschlüssel beim Entfernen der Anwendung zurückgelassen werden.

## <a name="selfreg-table"></a>Selfreg-Tabelle

Die Verwendung der Tabelle "selfreg" wird nicht empfohlen. Eine Liste der Gründe für die Verwendung der Selbstregistrierung finden Sie unter [selfreg Table](selfreg-table.md). Sie sollten stattdessen die Tabellen TypeLib, Klasse, AppID, ProgID, Extension, Verb und MIME verwenden, sofern möglich, und die Registrierungs Tabelle in allen anderen Fällen.

 

 



