---
title: Windows-Steuerelemente
description: Ein-Steuerelement ist ein untergeordnetes Fenster, das von einer Anwendung in Verbindung mit einem anderen Fenster zum Aktivieren der Benutzerinteraktion verwendet wird.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036567"
---
# <a name="windows-controls"></a>Windows-Steuerelemente

## <a name="purpose"></a>Zweck

Ein-Steuerelement ist ein untergeordnetes Fenster, das von einer Anwendung in Verbindung mit einem anderen Fenster zum Aktivieren der Benutzerinteraktion verwendet wird. Steuerelemente werden am häufigsten in Dialogfeldern verwendet, Sie können jedoch auch in anderen Fenstern verwendet werden. Steuerelemente in Dialogfeldern bieten dem Benutzer die Möglichkeit, Text einzugeben, Optionen auszuwählen und Aktionen zu initiieren. Steuerelemente in anderen Fenstern bieten eine Vielzahl von Diensten, z. b. das Auswählen von Befehlen, Anzeigen von Status und anzeigen und Bearbeiten von Text. Diese Dokumentation beschreibt die von Windows bereitgestellten Steuerelemente und die Programmier Elemente, die verwendet werden, um Sie zu erstellen und zu bearbeiten.

Eine Liste aller Windows-Steuerelemente, einschließlich eines Links zu umfassenden Übersichts-und Referenzinformationen für die einzelnen Steuerelemente, finden Sie unter [Steuerelement Bibliothek](individual-control-info.md).

## <a name="developer-audience"></a>Entwicklergruppe

Steuerelemente sind für die Verwendung durch C/C++-Entwickler und Benutzeroberflächen-Designer konzipiert. Im Allgemeinen benötigen Entwickler einen mittleren Einblick in die Programmier Konzepte der Benutzeroberfläche, die Windows-API-Programmierung und Unicode.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Unterstützung für Steuerelemente wird von User32.dll und Comctl32.dll bereitgestellt. Weitere Informationen finden Sie unter [allgemeine Steuerelement Versionen](common-control-versions.md).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                             | BESCHREIBUNG                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)<br/>                     | Bietet allgemeine Informationen, die allen Steuerelementen gemeinsam sind, die von Comctl32.dll unterstützt werden.<br/>                                      |
| [Steuern von Meldungen](control-messages.md)<br/>                               | Erläutert, wie Windows-Meldungen verwendet werden, um mit Steuerelementen zu kommunizieren.<br/>                                                                 |
| [Benutzerdefinierte Steuerelemente](user-controls-intro.md)<br/>                             | Beschreibt verschiedene Methoden zum Erstellen von benutzerdefinierten Steuerelementen. <br/>                                                                                 |
| [Subclassingsteuerelemente](subclassing-overview.md)<br/>                       | Beschreibt, wie Sie ein Steuerelement anpassen können, indem Sie seine Features ändern oder neue hinzufügen. <br/>                                                 |
| [Benutzerdefiniertes Zeichnen](custom-draw.md)<br/>                                         | Beschreibt einen Dienst, der von einigen Steuerelementen bereitgestellt wird und die Anwendungen verwenden können, um verschiedene Aspekte der Darstellung des Steuer Elements anzupassen. <br/> |
| [Überlegungen zur Sicherheit: Microsoft Windows-Steuerelemente](sec-comctls.md)<br/> | Enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows-Steuerelementen. <br/>                                                 |
| [Steuerelementbibliothek](individual-control-info.md)<br/>                         | Stellt Übersichten und Referenzinformationen zu jedem Steuerelement bereit, das von User32.dll und Comctl32.dll unterstützt wird.<br/>                            |
| [Allgemeine Steuerungs Referenz](common-control-reference.md)<br/>              | Bietet Referenzinformationen zu Programmier Elementen, die für mehrere Steuerelemente gelten, nicht nur für ein bestimmtes Steuerelement.<br/>           |
| [Control Spy v 2.0](control-spy.md)<br/>                                    | Beschreibt das Steuerelement Spy, ein Tool, das Entwicklern hilft, allgemeine Steuerelemente zu verstehen. <br/>                                                     |
| [Visuelle Stile](themes-overview.md)<br/>                                   | Beschreibt, wie die Darstellung von Steuerelementen je nach dem vom Benutzer ausgewählten visuellen Stil geändert werden kann. <br/>                               |
| [Designdatei Format](themesfileformat-overview.md)<br/>                     | Erläutert das Format der Designdateien (. Theme), die in Windows 7 und Windows Vista verwendet werden.<br/>                                                    |



 

 

 





