---
title: Integrieren von Schema Erweiterungen in die Benutzeroberfläche
description: Die Verwaltungs Tools von Active Directory Domain Services verwenden eine gängige Architektur zum Verbinden der administrativen Benutzeroberfläche mit dem Verzeichnisschema.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337961"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integrieren von Schema Erweiterungen in die Benutzeroberfläche

Die Verwaltungs Tools von Active Directory Domain Services verwenden eine gängige Architektur zum Verbinden der administrativen Benutzeroberfläche mit dem Verzeichnisschema. Das Kernstück dieser Architektur ist die **displaySpecifier** -Objektklasse. Anzeige spezifier und deren Verwendung werden ausführlich unter [Erweitern der Benutzeroberfläche für Verzeichnisobjekte](extending-the-user-interface-for-directory-objects.md)beschrieben.

Wenn Sie eine neue Klasse erstellen, indem Sie eine Unterklasse einer vorhandenen Klasse erstellen, können Sie die vorhandene Benutzeroberfläche für die übergeordnete Klasse nutzen, indem Sie den Anzeigespezifizierer der übergeordneten Klasse kopieren. Eine einfache Möglichkeit, den Anzeige Spezifizierer für eine Klasse zu kopieren, besteht darin, Sie mithilfe von LDIFDE in eine LDIF-Datei zu exportieren, den Distinguished Name und den CN zu bearbeiten und dann die geänderte LDIF-Datei zu importieren. Wenn die Unterklasse über zusätzliche Attribute verfügt, müssen Sie zusätzliche Eigenschaften Seiten bereitstellen, um die Bearbeitung zu unterstützen. Wenn die Unterklasse über zusätzliche erforderliche Eigenschaften verfügt, müssen Sie Erweiterungs Seiten für das Erstellen von Dialog Feld bereitstellen, da die von der übergeordneten Klasse bereitgestellte Benutzeroberfläche keine Möglichkeit zum Erstellen dieser neuen Attribute hat.

 

 




