---
description: Eine Geschäftsregel ermöglicht einer Anwendung die Verwendung von Logik zur Laufzeit, um berechtigungen zu qualifizieren, die dem Client erteilt wurden.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Geschäftsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54260fc6c7dd56137b3065a07f0dcccf9df1c4d21add4b9e7f0cfa79b0300e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783626"
---
# <a name="business-rules"></a>Geschäftsregeln

Eine Geschäftsregel ermöglicht einer Anwendung die Verwendung von Logik zur Laufzeit, um berechtigungen zu qualifizieren, die dem Client erteilt wurden.

Eine Geschäftsregel ist ein Skript, das in der Programmiersprache Visual Basic Scripting Edition (VBScript) oder mithilfe der Microsoft JScript-Entwicklungssoftware geschrieben wurde, die einem [**IAzTask-Objekt zugeordnet**](/windows/desktop/api/Azroles/nn-azroles-iaztask) ist. Wenn eine Anwendung den Zugriff auf einen Vorgang überprüft, überprüft der Autorisierungs-Manager zunächst, ob der aktuelle Client Zugriff auf Aufgaben hat, die diesen Vorgang enthalten, aber nicht mit Geschäftsregeln verknüpft sind. Wenn der Zugriff auf diese Weise nicht gewährt wird, führt der Autorisierungs-Manager Geschäftsregelskripts aus, die einer Aufgabe zugeordnet sind, die den Vorgang enthält.

Eine Anwendung übergibt Informationen als Arraypaar, das die Namen und Werte von Parametern darstellen, an ein Geschäftsregelskript. Das Skript hat Zugriff auf diese Parameter über ein [**AzBizRuleContext-Objekt,**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) das erstellt wird, wenn das Skript ausgeführt wird.

Ein Geschäftsregelskript kann nicht einem Task zugewiesen werden, der in einem delegierten Bereich enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Qualifizieren des Zugriffs mit Geschäftslogik in C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



