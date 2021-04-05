---
title: Grundlegendes zu Attribut Quellen
description: Grundlegendes zu Attribut Quellen
ms.assetid: 83274fea-233d-40dc-b587-99e99ddcd92b
keywords:
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b7266b75f8f506b1f06e822fbbb40a85d8f2dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713776"
---
# <a name="understanding-attribute-sources"></a>Grundlegendes zu Attribut Quellen

Die Attribute oder Metadaten, die Sie verwenden können, stammen aus einer Vielzahl von Quellen. Dieses Thema beschreibt diese Quellen und wechselt von Szenarien mit weniger potenziellen Attributen zu denjenigen mit mehr potenziellen Attributen.

Während der Benutzer eine CD oder DVD wieder gibt, haben Sie Zugriff auf sehr kleine Metadaten über die Festplatte selbst oder den Medieninhalt der Festplatte. Kommerzielle Scheiben enthalten in der Regel keine Attribut Metadaten.

Wenn der Benutzer eine CD oder DVD abgespielt hat, während er mit dem Internet verbunden war, haben Sie möglicherweise Zugriff auf weitere Attribute, wenn sich die Festplatte auf dem CD-oder DVD-Laufwerk befindet. Obwohl Windows Media Player mit dem Internet verbunden ist und eine CD oder DVD wieder gibt, ruft der Spieler die Metadaten für diese CD aus einer Online Datenbank ab. Der Player zeigt diese Informationen **jetzt** an und in einem separaten Knoten in der Bibliothek. Die Attribute werden nicht in der Bibliotheks Datenbank gespeichert, aber Sie werden zwischengespeichert. Wenn der Cache noch nicht geleert wurde, kann die Anwendung auf die Attribute zugreifen, während sich die Festplatte auf dem Laufwerk befindet.

> [!Note]  
> Benutzer können sich entscheiden, das Abrufen von Medieninformationen aus einer Online Datenbank zu deaktivieren. In diesem Fall sind die einzigen für Sie verfügbaren Attribute die aus einer digitalen Mediendatei, die Benutzer, die der Benutzer manuell in der Bibliothek eingegeben hat, und die, die vom Player selbst generiert wurden (z. b. die Attribute, die sich auf die Art der Wiedergabe eines Elements beziehen).

 

Wenn der Benutzer eine digitale Mediendatei wieder gibt, die nicht der Bibliothek hinzugefügt wurde, haben Sie Zugriff auf die Attribute, die in der Datei enthalten sind.

Wenn der Benutzer eine digitale Mediendatei wieder gibt, die der-Bibliothek hinzugefügt wurde, haben Sie Zugriff auf die Attribute, die nur in der-Bibliothek gespeichert sind, die Attribute, die nur in der-Datei gespeichert sind, und die Attribute, die in der-Bibliothek und in der-Datei gespeichert sind.

Die Attribute, die für die der Bibliothek hinzugefügten Medienelemente verfügbar sind, variieren je nach der Erstellung der digitalen Quell Mediendatei und den Aktionen, die der Benutzer seit dem Hinzufügen durchgeführt hat.

-   Der Ersteller des Inhalts kann bei der ersten Erstellung Attributinformationen in die Datei einfügen. Wenn Sie z. b. eine digitale Mediendatei mit Ihrer Anwendung erstellen und verteilen, können Sie steuern, welche Attribute ursprünglich in die Datei eingefügt wurden.
-   Wenn der Benutzer Attributdaten für ein Medien Element ändert, das der Bibliothek hinzugefügt wurde, indem der erweiterte TagEditor oder die Benutzeroberfläche der Bibliothek verwendet wird, werden diese Daten von Windows Media Player der Bibliotheks Datenbank hinzugefügt. Der Player fügt einige Attribute direkt der Datei hinzu, da Sie nur in der Datei gespeichert werden. Zu einem unbestimmten Zeitpunkt synchronisieren die Lese-/Schreibattribute mit der Datei, sodass Attribute, die sowohl in der Bibliothek als auch in der Datei gespeichert sind, denselben Wert aufweisen.
-   Wenn der Benutzer eine Spur mithilfe von Windows Media Player von einer CD kopiert, während eine Verbindung mit dem Internet besteht, ist der Effekt beinahe identisch mit dem Benutzer, der die Attribute mithilfe von Windows Media Player geändert hat. Attribute werden der Bibliotheks Datenbank hinzugefügt, die aus der Datei selbst und aus einer Online Datenbank gezeichnet werden. Einige Attribute werden nur in der Datei gespeichert. Zu einem unbestimmten Zeitpunkt wird die Bibliotheks Datenbank mit der Datei synchronisiert.
-   Wenn Sie Code mithilfe des Windows Media Player-Steuer Elements schreiben, um den Wert eines vorhandenen Lese-/schreibattributs in einem Medien Element zu ändern, das der Bibliothek hinzugefügt wurde, ist der Effekt beinahe identisch mit dem, wenn der Benutzer das Attribut mithilfe von Windows Media Player geändert hätte. Der Wert wird in die Bibliotheks Datenbank geschrieben, und die Datenbank wird zu einem unbestimmten Zeitpunkt mit der Datei synchronisiert.
-   [!Note]  
    > Wenn Sie das Steuerelement in Ihre Anwendung einbetten, werden Dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei selbst geschrieben, wenn der Benutzer Windows Media Player ausführt. Wenn Sie das-Steuerelement in einer Remote Anwendung verwenden, die in C++ geschrieben ist, werden die Dateiattribute, die Sie ändern, kurz nach dem vornehmen der Änderungen in die digitale Mediendatei geschrieben. In beiden Fällen sind die Änderungen sofort über die Bibliothek verfügbar.

     

-   Wenn Sie Code mithilfe des Windows Media Player-Steuer Elements schreiben, um ein benutzerdefiniertes Attribut in ein Medien Element einzufügen, werden das Attribut und sein Wert nur so lange beibehalten, wie die Anwendung einen Verweis auf das **Medien** Objekt aufweist. Das Attribut und sein Wert werden in der Bibliotheks Datenbank oder der digitalen Mediendatei (sofern vorhanden) nicht gespeichert.

Die einfachste Situation ist, wenn Sie mit digitalen Mediendateien arbeiten, die Sie bereitgestellt haben. In diesem Szenario wissen Sie, dass sich bestimmte Attribute in der Datei befinden. Wenn Sie das Medien Element der Bibliothek hinzufügen, wissen Sie, dass Sie mit diesen Attributen arbeiten können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medien Element Attribute**](media-item-attributes.md)
</dt> </dl>

 

 




