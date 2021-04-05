---
title: Ihren Peer nicht als vertrauenswürdig einstufen
description: '\ 0034; dem Peer nicht Vertrauen \ 0034; ist eine grundlegende Sicherheitsregel, die jedoch oft übersehen wird.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709965"
---
# <a name="do-not-trust-your-peer"></a>Ihren Peer nicht als vertrauenswürdig einstufen

"Ihr Peer nicht als vertrauenswürdig einstufen" ist eine grundlegende Sicherheitsregel, die jedoch oft übersehen wird. Gehen Sie nicht davon aus, dass sich die andere Partei in einer Kommunikation ordnungsgemäß verhält, und gehen Sie nicht davon aus, dass Ihr Peer die erwarteten Daten übergibt. In der Mitte und in RPC werden in Ihrem Namen einige Überprüfungen durchgeführt, aber nicht alle Prüfungen.

Stellen Sie fest, welcher Aspekt der Parameter von "Mittel l" oder "RPC" überprüft wird und welche Aspekte Sie selbst überprüfen müssen. Beispielsweise prüft RPC bei in/out-Kontext Handles, ob das Kontext Handle kein Ungültiger Wert ungleich NULL ist. Sie lässt NULL-Werte und gültige Werte zu, aber viele Entwickler sind nicht darauf aufmerksam, dass NULL-Werte durchgelassen werden. Dies soll überprüft werden.

Selbst wenn Sie Ihrem Peer im allgemeinen Vertrauen, stellen Sie sicher, dass keine neuen Pfade eingeführt werden, mit denen ein kompromittiertes Computer-oder Prinzipal Konto andere Computer angreifen kann. Angenommen, ein Benutzer wählt seinen Geburtstag als Kennwort aus, und er wird von einem Angreifer erraten. Auch nachdem Anforderungen des Benutzers authentifiziert wurden und der Zugriff auf seine Daten zulässig ist, stellen Sie sicher, dass keine ausnutzbaren Sicherheitsrisiken vorhanden sind. diese Stapel Überläufe können einem Angreifer ermöglichen, die Kontrolle über den Server zu übernehmen und die Sicherheitsverletzung zu verlängern.

 

 




