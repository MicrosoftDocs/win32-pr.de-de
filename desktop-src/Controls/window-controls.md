---
title: Windows Steuerelemente
description: Ein Steuerelement ist ein untergeordnetes Fenster, das eine Anwendung in Verbindung mit einem anderen Fenster verwendet, um die Benutzerinteraktion zu ermöglichen.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bbf1c7ebf33b5665b086b34dd7134cdebadc299f4e2010710ddf4ae519dc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957539"
---
# <a name="windows-controls"></a>Windows Steuerelemente

## <a name="purpose"></a>Zweck

Ein Steuerelement ist ein untergeordnetes Fenster, das eine Anwendung in Verbindung mit einem anderen Fenster verwendet, um die Benutzerinteraktion zu ermöglichen. Steuerelemente werden am häufigsten in Dialogfeldern verwendet, können aber auch in anderen Fenstern verwendet werden. Steuerelemente in Dialogfeldern bieten dem Benutzer die Möglichkeit, Text ein- und auswählen und Aktionen initiieren zu können. Steuerelemente in anderen Fenstern bieten eine Vielzahl von Diensten, z. B. die Auswahl von Befehlen, das Anzeigen des Status und das Anzeigen und Bearbeiten von Text. In dieser Dokumentation werden die steuerelemente, die von Windows bereitgestellt werden, und die Programmierelemente beschrieben, mit deren Hilfe sie erstellt und bearbeitet werden.

Eine Liste aller Steuerelemente Windows, einschließlich eines Links zu einer umfassenden Übersicht und Referenzinformationen für jedes Steuerelement, finden Sie unter [Control Library](individual-control-info.md).

## <a name="developer-audience"></a>Entwicklergruppe

Steuerelemente sind für die Verwendung durch C/C++-Entwickler und Benutzeroberflächen-Designer konzipiert. Im Allgemeinen benötigen Entwickler ein mittleres Maß an Kenntnissen zu Konzepten der Benutzeroberflächenprogrammierung, Windows API-Programmierung und Unicode.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Unterstützung für Steuerelemente wird von User32.dll und Comctl32.dll. Weitere Informationen finden Sie unter [Allgemeine Steuerelementversionen.](common-control-versions.md)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                             | Beschreibung                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)<br/>                     | Stellt allgemeine Informationen zur Verfügung, die allen Steuerelementen gemeinsam sind, die von der Comctl32.dll.<br/>                                      |
| [Steuern von Nachrichten](control-messages.md)<br/>                               | Erläutert, Windows Nachrichten für die Kommunikation mit Steuerelementen verwendet werden.<br/>                                                                 |
| [Benutzerdefinierte Steuerelemente](user-controls-intro.md)<br/>                             | Beschreibt verschiedene Möglichkeiten zum Erstellen benutzerdefinierter Steuerelemente. <br/>                                                                                 |
| [Steuerelemente für Unterklassen](subclassing-overview.md)<br/>                       | Beschreibt eine Möglichkeit, ein Steuerelement anzupassen, indem seine Features geändert oder neue hinzugefügt werden. <br/>                                                 |
| [Benutzerdefiniertes Zeichnen](custom-draw.md)<br/>                                         | Beschreibt einen Dienst, der von einigen Steuerelementen bereitgestellt wird und mit dem Anwendungen verschiedene Aspekte der Darstellung des Steuerelements anpassen können. <br/> |
| [Sicherheitsüberlegungen: Microsoft Windows Controls](sec-comctls.md)<br/> | Enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows Steuerelementen. <br/>                                                 |
| [Steuerelementbibliothek](individual-control-info.md)<br/>                         | Stellt Übersichten und Referenzinformationen zu den einzelnen Steuerelementen zur Verfügung, die von User32.dll und Comctl32.dll.<br/>                            |
| [Allgemeine Steuerelementreferenz](common-control-reference.md)<br/>              | Stellt Referenzinformationen zu Programmierelementen zur Verfügung, die nicht nur für ein bestimmtes Steuerelement, sondern auch für mehrere Steuerelemente gelten.<br/>           |
| [Steuern von Spy v2.0](control-spy.md)<br/>                                    | Beschreibt Control Spy, ein Tool, das Entwicklern hilft, allgemeine Steuerelemente zu verstehen. <br/>                                                     |
| [Visuelle Stile](themes-overview.md)<br/>                                   | Beschreibt, wie sich die Darstellung von Steuerelementen je nach dem vom Benutzer ausgewählten visuellen Stil ändern kann. <br/>                               |
| [Designdateiformat](themesfileformat-overview.md)<br/>                     | Erläutert das Format von Designdateien (.theme), die in Windows 7 und Windows Vista verwendet werden.<br/>                                                    |



 

 

 





