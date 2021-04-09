---
title: Sonstige RPC-Leistungs Tipps
description: In diesem Abschnitt werden verschiedene Leistungs Tipps zum Entwickeln von leistungsstarken RPC-Servern erläutert. Dieser Abschnitt enthält viele Tipps, die sich auf den RPC-Client beziehen. Wenn Sie einen RPC-Client ordnungsgemäß entwickeln, kann der RPC-Server weniger Arbeit ausführen.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036595"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Sonstige RPC-Leistungs Tipps

In diesem Abschnitt werden verschiedene Leistungs Tipps zum Entwickeln von leistungsstarken RPC-Servern erläutert. Dieser Abschnitt enthält viele Tipps, die sich auf den RPC-Client beziehen. Wenn Sie einen RPC-Client ordnungsgemäß entwickeln, kann der RPC-Server weniger Arbeit ausführen.

## <a name="use-kerberos"></a>Verwenden von Kerberos

Wenn Sicherheit verwendet wird, verwenden Sie Kerberos. Auf der Serverseite ist für Kerberos kein Zugriff auf den KDC erforderlich. Dadurch wird die Arbeitsauslastung vom Server auf den Client verlagert, der Server mit besserer Leistung bereitstellt.

## <a name="use-static-identity-tracking"></a>Statische Identitäts Überwachung verwenden

Wenn Sicherheit verwendet wird, versuchen Sie, die statische Identitäts Überwachung zu verwenden. Die statische Identitäts Verfolgung ist im Hinblick auf die Ressourcenverwendung günstiger als die dynamische Identitäts Überwachung. Wenn sich die Client Identität ändert und der Server die Änderung nicht beachten sollte, verwenden Sie die dynamische Überwachung, anstatt ein anderes Bindungs Handle für jede Identität zu erstellen. Wenn die Identität jedoch identisch ist, sollten Sie sicherstellen, dass RPC diese Tatsache kennt, um zu vermeiden, dass die RPC-Überprüfung auf geänderte Identitäten jedes Mal erfolgt.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Verwenden der rpcgetauthorizationcontextforclient-Funktion

Wenn Sie den Zugriff unter Windows XP überprüfen müssen, verwenden Sie die Funktion [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) . Die sich ergebenden Authz-Kontexte ermöglichen sehr schnelle Zugriffs Überprüfungen, die von der RPC-Laufzeit effizient zwischengespeichert werden.

## <a name="do-not-modify-the-token-unless-necessary"></a>Ändern Sie das Token nur, wenn dies erforderlich ist.

Wenn die dynamische Identitäts Verfolgung verwendet wird, sollten Sie das Thread-/Prozesstoken nur ändern, wenn dies unbedingt erforderlich ist. Auch wenn es in Einstellungen geändert wird, die es zuvor gab, unterscheidet sich das Token oft ausreichend vom Sicherheitssystem, um die Einrichtung eines neuen Sicherheits Kontexts zu initiieren.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Die Serialisierung im gemischten Modus für Kontext Handles wird berücksichtigt.

Der standardserialisierungsmodus für das Kontext Handle wird serialisiert (exklusiv). Erstellen Sie ggf. alle Aufrufe, die den Zustand des Kontext Handles nicht ändern, im freigegebenen Serialisierungsmodus. Weitere Informationen finden Sie unter [**rpcsscontextlockexclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) .

 

 




