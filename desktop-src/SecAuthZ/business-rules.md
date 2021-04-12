---
description: Eine Geschäftsregel ermöglicht einer Anwendung die Verwendung von Logik zur Laufzeit, um dem Client gewährte Berechtigungen zu qualifizieren.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Geschäftsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218830"
---
# <a name="business-rules"></a>Geschäftsregeln

Eine Geschäftsregel ermöglicht einer Anwendung die Verwendung von Logik zur Laufzeit, um dem Client gewährte Berechtigungen zu qualifizieren.

Eine Geschäftsregel ist ein Skript, das in der Programmiersprache Visual Basic Scripting Edition (VBScript) geschrieben oder mithilfe der Microsoft JScript-Entwicklungssoftware geschrieben wurde, die einem [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt zugeordnet ist. Wenn eine Anwendung den Zugriff auf einen Vorgang überprüft, prüft der Autorisierungs-Manager zunächst, ob der aktuelle Client Zugriff auf Tasks hat, die diesen Vorgang enthalten, aber nicht mit Geschäftsregeln verknüpft sind. Wenn der Zugriff auf diese Weise nicht gewährt wird, führt der Autorisierungs-Manager Geschäftsregel Skripts aus, die einer Aufgabe zugeordnet sind, die den Vorgang enthält.

Eine Anwendung übergibt Informationen als Paar von Arrays, die die Namen und Werte von Parametern darstellen, an ein Geschäftsregel Skript. Das Skript hat Zugriff auf diese Parameter über ein [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) -Objekt, das beim Ausführen des Skripts erstellt wird.

Einem Task, der in einem Delegierten Bereich enthalten ist, kann kein Geschäftsregel Skript zugewiesen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Qualifizieren des Zugriffs mit Geschäftslogik in C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



