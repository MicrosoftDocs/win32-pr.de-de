---
description: Besondere Überlegungen müssen für mehrfach vernetzte PGM-Absender oder-Empfänger angegeben werden. Auf dieser Seite werden die Überlegungen beschrieben und Richtlinien für Best Practices für die Programmierung bereitstellt.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multihosting und PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347164"
---
# <a name="multihoming-and-pgm"></a>Multihosting und PGM

Besondere Überlegungen müssen für mehrfach vernetzte PGM-Absender oder-Empfänger angegeben werden. Auf dieser Seite werden die Überlegungen beschrieben und Richtlinien für Best Practices für die Programmierung bereitstellt.

## <a name="multihomed-pgm-sender"></a>Mehrfach vernetzter PGM-Sender

Wenn eine Anwendung beim Aufrufen der [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion keine Schnittstelle angibt, wird die erste verfügbare Schnittstelle verwendet. Wenn keine Schnittstelle verfügbar ist, schlägt die **Verbindungs** Herstellung fehl.

Wenn eine Anwendung mithilfe der Option [RM \_ Set \_ Send \_ if](socket-options.md) Socket eine Schnittstelle angibt, wird ein [**Bindungs**](/windows/desktop/api/winsock/nf-winsock-bind) Versuch implizit an diese Schnittstelle mithilfe von TCP/IP vorgenommen und schlägt fehl, wenn TCP/IP die Bindungs Anforderung nicht erfüllt. Wenn die Schnittstelle mithilfe von RM \_ Set \_ Send \_ , wenn mehrmals festgelegt wird, gilt nur die letzte erfolgreich festgelegte Schnittstelle.

Windows Sockets verwaltet, welche Schnittstelle festgelegt ist. wenn diese Schnittstelle nicht mehr angezeigt wird, wird die Sitzung getrennt.

## <a name="multihomed-pgm-receiver"></a>Mehrfach vernetzter PGM-Empfänger

Wenn eine Anwendung beim Aufrufen der Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " keine Schnittstelle angibt, wird die Standardschnittstelle verwendet. Wenn keine Schnittstelle verfügbar ist, schlägt [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) fehl.

Wenn eine Anwendung eine oder mehrere Schnittstellen angibt, auf die gelauscht werden soll, wird bei Verwendung von [RM \_ Add \_ Receive \_ if](socket-options.md)der Versuch unternommen, mit TCP/IP eine Bindung an die angeforderte Schnittstelle herzustellen. Jeder Fehler von TCP/IP bewirkt, dass diese Anforderung fehlschlägt. Anders als bei der PGM-Absender Anfrage führt das Hinzufügen einer Empfangs Schnittstelle mehrmals dazu, dass auf allen erfolgreich hinzugefügten Schnittstellen lauscht. Verwenden Sie die \_ Option RM del \_ Receive \_ if Socket, um das lauschen an einer Schnittstelle zu beenden.

Windows Sockets behält den Zustand über mehrere angegebene Überwachungsschnittstellen bei und basiert stattdessen auf TCP/IP. Sobald eine Sitzung ausgeführt wird, verfolgt Windows Sockets jedoch die eingehende Schnittstelle für diese Sitzung. wenn diese Schnittstelle nicht mehr angezeigt wird, trennt Windows Sockets die Sitzung.

 

 



