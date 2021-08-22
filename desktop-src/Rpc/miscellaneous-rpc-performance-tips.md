---
title: Verschiedene RPC-Tipps
description: In diesem Abschnitt werden verschiedene Leistungstipps für die Entwicklung von RPC-Hochleistungsservern erläutert. Dieser Abschnitt enthält viele Tipps, die sich auf den RPC-Client beziehen. Durch die ordnungsgemäße Entwicklung eines RPC-Clients kann der RPC-Server weniger Aufgaben ausführen.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0946b83aae296f7b908babca9135c35a0afe8dbe7588a8292ad66bc19dc6488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928069"
---
# <a name="miscellaneous-rpc-performance-tips"></a>Verschiedene RPC-Tipps

In diesem Abschnitt werden verschiedene Leistungstipps für die Entwicklung von RPC-Hochleistungsservern erläutert. Dieser Abschnitt enthält viele Tipps, die sich auf den RPC-Client beziehen. Durch die ordnungsgemäße Entwicklung eines RPC-Clients kann der RPC-Server weniger Aufgaben ausführen.

## <a name="use-kerberos"></a>Verwenden von Kerberos

Wenn Sicherheit verwendet wird, verwenden Sie Kerberos. Auf Serverseite erfordert Kerberos keinen Zugriff auf das KDC. Dadurch wird die Arbeitsauslastung vom Server auf den Client übertragen, was eine bessere Leistung von Servern bietet.

## <a name="use-static-identity-tracking"></a>Verwenden der statischen Identitätsnachverfolgung

Wenn Sicherheit verwendet wird, versuchen Sie, die statische Identitätsnachverfolgung zu verwenden. Die statische Identitätsnachverfolgung ist im Hinblick auf die Ressourcennutzung kostengünstiger als die dynamische Identitätsnachverfolgung. Wenn sich die Clientidentität ändert und der Server die Änderung nicht beachten sollte, verwenden Sie die dynamische Nachverfolgung, anstatt ein anderes Bindungshand handle für jede Identität zu erstellen. Wenn die Identität jedoch identisch ist, stellen Sie sicher, dass RPC diese Tatsache kennt, um zu vermeiden, dass RPC jedes Mal Überprüfungen auf geänderte Identitäten vor sich hat.

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a>Verwenden der RpcGetAuthorizationContextForClient-Funktion

Wenn Sie den Zugriff in Windows XP überprüfen müssen, verwenden Sie die [**RpcGetAuthorizationContextForClient-Funktion.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) Die resultierenden Rpchz-Kontexte ermöglichen sehr schnelle Zugriffsüberprüfungen, die von der RPC-Laufzeit effizient zwischengespeichert werden.

## <a name="do-not-modify-the-token-unless-necessary"></a>Ändern Sie das Token nur, wenn dies erforderlich ist.

Wenn die dynamische Identitätsnachverfolgung verwendet wird, ändern Sie das Thread-/Prozesstoken nur, wenn dies unbedingt erforderlich ist. Selbst wenn es in Einstellungen geändert wurde, die es zuvor hatte, ist das Token oft ausreichend anders als das Sicherheitssystem, um die Einrichtung eines neuen Sicherheitskontexts auszulösen.

## <a name="consider-mixed-mode-serialization-for-context-handles"></a>Erwägen der Serialisierung im gemischten Modus für Kontexthandles

Der Standardmäßige Serialisierungsmodus für das Kontexthand handle wird serialisiert (exklusiv). Erwägen Sie, alle Aufrufe zu tätigen, die den Zustand des Kontexthandpunkts im freigegebenen Serialisierungsmodus nicht ändern. Weitere Informationen finden Sie unter [**RpcSsContextLockExclusive.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive)

 

 




