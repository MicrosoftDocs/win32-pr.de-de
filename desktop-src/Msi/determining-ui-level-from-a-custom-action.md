---
description: Für eine benutzerdefinierte Aktion in einer UI-Sequenz Tabelle oder einer externen ausführbaren Datei ist möglicherweise die aktuelle Benutzeroberflächen Ebene der Installation erforderlich.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960060"
---
# <a name="determining-ui-level-from-a-custom-action"></a>Bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion

Für eine benutzerdefinierte Aktion in einer UI-Sequenz Tabelle oder einer externen ausführbaren Datei ist möglicherweise die aktuelle Benutzeroberflächen Ebene der Installation erforderlich. Beispielsweise sollte eine benutzerdefinierte Aktion mit einem Dialogfeld nur das Dialogfeld anzeigen, wenn es sich bei der Benutzeroberflächen Ebene um eine vollständige Benutzeroberfläche oder um eine reduzierte Benutzeroberfläche handelt. das Dialogfeld sollte nicht angezeigt werden, wenn die Benutzeroberflächen Ebene eine einfache Benutzeroberfläche oder keine Sie sollten die [**uilevel**](uilevel.md) -Eigenschaft verwenden, um die aktuelle Benutzeroberflächen Ebene zu bestimmen. Sie können [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) nicht aus einer benutzerdefinierten Aktion aufrufen, und es ist nicht möglich, die UI-Ebenen-Eigenschaft in einer benutzerdefinierten Aktion zu ändern.

Es wird empfohlen, dass benutzerdefinierte Aktionen nicht die Benutzeroberflächen Ebene als Bedingung für das Senden von Fehlermeldungen an das Installationsprogramm verwenden, da dies die Protokollierung und externe Nachrichten beeinträchtigen kann.

 

 



