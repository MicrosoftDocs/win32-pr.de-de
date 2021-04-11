---
title: Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen
description: Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206648"
---
# <a name="scripting-com-objects-in-custom-applications"></a>Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen

Microsoft stellt verschiedene Umgebungen für Skripterstellung für COM-Objekte bereit: Active Server Seiten, Windows Script Host usw. Unabhängige Softwarehersteller (ISVs) können auch Microsoft Scripting Engines für die Verwendung in Ihren Anwendungen lizenzieren. Beispielsweise könnte ein ISV, der einen Textverarbeitungs Text erstellt, der Anwendung eine Makrosprache hinzufügen, damit Benutzer einfache Aufgaben automatisieren können. Durch die Lizenzierung einer Skript-Engine kann der ISV eine Sprache wie VBScript oder JScript als Makrosprache der Anwendung verwenden.

Zusätzlich zur Lizenzierung von VBScript und JScript-Skript Modulen können ISVs eigene ActiveX-Skript-Engines schreiben. Diese Skript Module können dann an jede Host Umgebung angeschlossen werden, die den ActiveX-Skript-Engine-Standard unterstützt. Ein ISV könnte z. b. eine PerlScript-Skript-Engine schreiben und auf einem ASP-Server installieren, sodass der ASP-Server Perl Script-Skripts verarbeiten kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung mit COM-Objekten](scripting-with-com-objects.md)
</dt> </dl>

 

 




