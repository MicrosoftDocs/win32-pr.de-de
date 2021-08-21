---
description: Mehrfachstarts von PGM-Absendern oder -Empfängern müssen besonders berücksichtigt werden. Diese Seite beschreibt die Überlegungen und enthält Richtlinien für bewährte Programmiermethoden.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multihoming und PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e19ab149c8068c1a13f2c8089a567157618ef7287e8ef632145e5b934d626c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112084"
---
# <a name="multihoming-and-pgm"></a>Multihoming und PGM

Mehrfachstarts von PGM-Absendern oder -Empfängern müssen besonders berücksichtigt werden. Diese Seite beschreibt die Überlegungen und enthält Richtlinien für bewährte Programmiermethoden.

## <a name="multihomed-pgm-sender"></a>Mehrfach vernetzter PGM-Absender

Wenn eine Anwendung beim Aufrufen der [**connect-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-connect) keine Schnittstelle angeben kann, wird die erste verfügbare Schnittstelle verwendet. Wenn keine Schnittstelle verfügbar ist, schlägt die **Verbindung** fehl.

Wenn eine Anwendung eine Schnittstelle mithilfe der [RM \_ SET SEND \_ \_ IF-Socketoption](socket-options.md) angibt, wird implizit ein [**Bindungsversuch**](/windows/desktop/api/winsock/nf-winsock-bind) an diese Schnittstelle unter Verwendung von TCP/IP durchgeführt, und es tritt ein Fehler auf, wenn TCP/IP bei der Bindungsanforderung fehlschlägt. Wenn die Schnittstelle mit RM SET SEND IF mehrmals festgelegt \_ \_ \_ wird, ist nur der letzte Schnittstellensatz erfolgreich anwendbar.

Windows Sockets verwaltet, welche Schnittstelle festgelegt ist, und wenn diese Schnittstelle nicht mehr angezeigt wird, wird die Sitzung getrennt.

## <a name="multihomed-pgm-receiver"></a>Mehrfach vernetzter PGM-Empfänger

Wenn eine Anwendung beim Aufrufen der [**Listenfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-listen) keine Schnittstelle angeben kann, wird die Standardschnittstelle verwendet. Wenn keine Schnittstelle verfügbar ist, schlägt [**die Bindung**](/windows/desktop/api/winsock/nf-winsock-bind) fehl.

Wenn eine Anwendung eine oder mehrere Schnittstellen angibt, an denen geleert werden soll, versucht Windows Sockets mithilfe von [RM \_ ADD RECEIVE \_ \_ IF,](socket-options.md)eine Bindung an die angeforderte Schnittstelle oder Schnittstellen über TCP/IP zu erstellen. Jeder Tcp/IP-Fehler führt dazu, dass diese Anforderung fehlschlägt. Im Gegensatz zum Fall des PGM-Absenders führt das mehrmalige Hinzufügen einer Empfangsschnittstelle dazu, dass die Lauschen an allen erfolgreich hinzugefügten Schnittstellen gesendet werden. Verwenden Sie die \_ RM DEL \_ RECEIVE \_ IF-Socketoption, um die Überwachung einer Schnittstelle zu beenden.

Windows Sockets behalten nicht den Zustand mehrerer angegebener Lauschenschnittstellen bei und verwenden dafür TCP/IP. Sobald jedoch eine Sitzung ausgeführt wird, verfolgen Windows Sockets die eingehende Schnittstelle für diese Sitzung nach. Wenn diese Schnittstelle nicht mehr angezeigt wird, trennt Windows Sockets die Sitzung.

 

 



