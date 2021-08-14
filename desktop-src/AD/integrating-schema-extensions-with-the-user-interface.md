---
title: Integrieren von Schemaerweiterungen in die Benutzeroberfläche
description: Die Verwaltungstools von Active Directory Domain Services eine allgemeine Architektur verwenden, um die Administrative Benutzeroberfläche mit dem Verzeichnisschema zu verbinden.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d951ec51d7453ee92cf90ddcb28ddb8219d3056b1edb96d16bf15494fe956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187209"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integrieren von Schemaerweiterungen in die Benutzeroberfläche

Die Verwaltungstools von Active Directory Domain Services eine allgemeine Architektur verwenden, um die Administrative Benutzeroberfläche mit dem Verzeichnisschema zu verbinden. Das Kernstück dieser Architektur ist die **displaySpecifier-Objektklasse.** Anzeigespezifizierer und ihre Verwendung werden unter [Erweitern der Benutzeroberfläche für Verzeichnisobjekte](extending-the-user-interface-for-directory-objects.md)ausführlich beschrieben.

Wenn Sie eine neue Klasse erstellen, indem Sie eine vorhandene Klasse untergliedern, können Sie die vorhandene Benutzeroberfläche für die Übergeordnete Klasse nutzen, indem Sie den Anzeigespezifizierer der Übergeordneten Klasse kopieren. Eine einfache Möglichkeit, den Anzeigespezifizierer für eine Klasse zu kopieren, besteht darin, ihn mit LDIFDE in eine LDIF-Datei zu exportieren, den Distinguished Name und den CN zu bearbeiten und dann die geänderte LDIF-Datei zu importieren. Wenn die Unterklasse über zusätzliche Attribute verfügt, müssen Sie zusätzliche Eigenschaftenseiten bereitstellen, um die Bearbeitung zu unterstützen. Wenn die Unterklasse über zusätzliche Must-Have-Eigenschaften verfügt, müssen Sie Erweiterungsseiten für das Erstellungsdialogfeld bereitstellen, da die von der Übergeordneten Klasse bereitgestellte Benutzeroberfläche keine Möglichkeit hat, diese neuen Attribute zu erstellen.

 

 




