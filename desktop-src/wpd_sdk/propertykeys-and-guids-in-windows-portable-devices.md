---
description: PropertyKeys und GUIDs auf tragbaren Windows-Geräten
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PropertyKeys und GUIDs auf tragbaren Windows-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866507"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PropertyKeys und GUIDs auf tragbaren Windows-Geräten

Eine Eigenschaft oder ein Befehl wird durch eine PropertyKey-Struktur identifiziert. Eine PropertyKey-Struktur besteht aus zwei Teilen: einer GUID (dem fmtid-Member) und einem DWORD (dem PID-Member). Der GUID-Teil wird verwendet, um die Kategorie anzugeben, zu der die Eigenschaft oder der Befehl gehört (d. h. verknüpfte Eigenschaften gehören derselben Kategorie, und zugehörige Befehle gehören derselben Kategorie an. Deshalb haben Sie dieselbe fmtid). Der DWORD-Teil gibt die Eigenschaft oder Befehls-ID an und wird verwendet, um die einzelnen Eigenschaften oder Befehle innerhalb einer Eigenschaft oder Befehls Kategorie zu unterscheiden (d. h., die PID-Werte für Eigenschaften oder Befehle in derselben Kategorie werden unterschiedlich sein).

Der Referenz Abschnitt dieses Dokuments beschreibt alle PropertyKey-Werte, die von WPD definiert werden. Diese Werte entsprechen Befehlen, Eigenschaften und Ressourcen. Wenn Sie einen benutzerdefinierten PropertyKey-Wert erstellen, sollten Sie eine neue **GUID** -Kategorie definieren. Verwenden Sie die WPD- **GUID** -Werte nicht, oder Sie riskieren einen Konflikt mit vorhandenen und zukünftigen WPD-spezifischen PropertyKeys.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungs Übersicht**](application-overview.md)
</dt> <dt>

[**Befehle**](commands.md)
</dt> <dt>

[**Objekt Format-GUIDs**](object-format-guids.md)
</dt> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



