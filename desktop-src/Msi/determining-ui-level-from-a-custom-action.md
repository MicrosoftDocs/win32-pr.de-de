---
description: Eine benutzerdefinierte Aktion in einer Benutzeroberflächensequenztabelle oder einer externen ausführbaren Datei benötigt möglicherweise die aktuelle Benutzeroberflächesebene der Installation.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Bestimmen der Benutzeroberflächenebene aus einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af88753b5ea44927ac58b13bcb4742e7992e50e1499aa04964b60b632d68ec53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947567"
---
# <a name="determining-ui-level-from-a-custom-action"></a>Bestimmen der Benutzeroberflächenebene aus einer benutzerdefinierten Aktion

Eine benutzerdefinierte Aktion in einer Benutzeroberflächensequenztabelle oder einer externen ausführbaren Datei benötigt möglicherweise die aktuelle Benutzeroberflächesebene der Installation. Beispielsweise sollte eine benutzerdefinierte Aktion, die über ein Dialogfeld verfügt, das Dialogfeld nur anzeigen, wenn die Benutzeroberflächesebene vollständig oder Reduzierte Benutzeroberfläche ist. Sie sollte das Dialogfeld nicht anzeigen, wenn die Benutzeroberflächenebene Basic UI oder None ist. Sie sollten die [**UILevel-Eigenschaft**](uilevel.md) verwenden, um die aktuelle Benutzeroberflächesebene zu bestimmen. Sie können [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) nicht aus einer benutzerdefinierten Aktion aufrufen, und es ist nicht möglich, die Eigenschaft auf Benutzeroberflächenebene innerhalb einer benutzerdefinierten Aktion zu ändern.

Es wird empfohlen, dass benutzerdefinierte Aktionen die Benutzeroberflächenebene nicht als Bedingung für das Senden von Fehlermeldungen an das Installationsprogramm verwenden, da dies die Protokollierung und externe Meldungen beeinträchtigen kann.

 

 



