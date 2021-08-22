---
description: Der Dateityp des semantischen Typs ist einer der Schlüsselformattypen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Dateitabelle.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7611cce64bfe036575ac611ebbf63406721085f75162b04e9163eb38840cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581750"
---
# <a name="file-type"></a>Dateityp

Der Dateityp des [semantischen Typs](semantic-types.md) ist einer der [Schlüsselformattypen.](key-format-types.md) Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Dateitabelle.](file-table.md)

Der Dateityp kann mit den folgenden Arten von ContextData verwendet werden.

**AssemblyContext ContextData**

Dieser Typ kann verwendet werden, um Benutzern das Konfigurieren von Fremdschlüsseln für Win32- oder Common Language Runtime-Assemblys zu ermöglichen. Das Mergetool muss einen Windows [Installer-Bezeichner](identifier.md) für Elemente dieses Typs in die Vorlage in der Spalte Wert der [Tabelle ModuleSubs extensions](modulesubstitution-table.md)einfügen. Mergemod.dll erzwingt dies nicht, und das Zusammenführungstool muss sicherstellen, dass der Benutzer einen gültigen Schlüssel in der Dateitabelle bereitstellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, msmConfigItemNonNullable wurde in das Feld Attributes der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)eingefügt.

 

 



