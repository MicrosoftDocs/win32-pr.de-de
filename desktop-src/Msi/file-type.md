---
description: Der Dateityp des semantischen Typs ist einer der Schlüssel Format Typen. Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten Dateitabelle.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364096"
---
# <a name="file-type"></a>Dateityp

Der Dateityp des [semantischen Typs](semantic-types.md) ist einer der [Schlüssel Format Typen](key-format-types.md). Dieser Typ besteht aus einem Fremdschlüssel in der vom Benutzer bereitgestellten [Dateitabelle](file-table.md) .

Der Dateityp kann mit den folgenden Arten von ContextData verwendet werden.

**Assemblycontext ContextData**

Dieser Typ kann verwendet werden, um es Benutzern zu ermöglichen, Fremdschlüssel für Win32-oder Common Language Runtime Assemblys zu konfigurieren. Das Merge-Tool muss einen Windows Installer [Bezeichner](identifier.md) für Elemente dieses Typs in die Vorlage in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)ersetzen. Mergemod.dll erzwingt dies nicht, und es liegt an dem Merge-Tool, sicherzustellen, dass der Benutzer einen gültigen Schlüssel für die Dateitabelle bereitstellt.

NULL ist ein gültiger Wert für diesen Typ, es sei denn, der msmconfigitemnonable-Wert ist im Feld Attribute der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)enthalten.

 

 



