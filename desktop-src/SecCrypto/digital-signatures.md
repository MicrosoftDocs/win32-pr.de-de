---
description: Digitale Signaturen können verwendet werden, um eine Nachricht in nur-Text-Form zu verteilen, wenn die Empfänger den Absender der Nachricht identifizieren und überprüfen müssen.
ms.assetid: 10c33787-72d3-4e5d-b4dd-633b3fd29903
title: Digitale Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d84d1a1c71b6b6d709dbe67b4fa2c81f4b54e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128789"
---
# <a name="digital-signatures"></a>Digitale Signaturen

[*Digitale Signaturen*](../secgloss/d-gly.md) können verwendet werden, um eine Nachricht in nur-Text [*-Form zu*](../secgloss/p-gly.md) verteilen, wenn die Empfänger den Absender der Nachricht identifizieren und überprüfen müssen. Durch das Signieren einer Nachricht wird die Nachricht nicht geändert. Es generiert einfach eine digitale Signatur Zeichenfolge, die Sie entweder mit der Nachricht bündeln oder separat übertragen können. Eine digitale Signatur ist ein kurzes Datenelement, das mit dem [*privaten Schlüssel*](../secgloss/p-gly.md)des Absenders verschlüsselt ist. Durch das Entschlüsseln der Signatur Daten mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) des Absenders wird bestätigt, dass die Daten vom Absender oder von einem Benutzer mit Zugriff auf den privaten Schlüssel des Absenders verschlüsselt wurden.

Digitale Signaturen werden mithilfe von Signatur Algorithmen für [*öffentliche Schlüssel*](../secgloss/p-gly.md) generiert. Ein [*privater Schlüssel*](../secgloss/p-gly.md) generiert die Signatur, und der entsprechende öffentliche Schlüssel muss zum Überprüfen der Signatur verwendet werden. Dieser Vorgang wird in der folgenden Abbildung dargestellt.

![Erstellen einer digitalen Signatur](images/capi02.png)

Zum Erstellen einer digitalen Signatur aus einer Nachricht müssen zwei Schritte ausgeführt werden. Der erste Schritt umfasst das Erstellen eines [*Hashwerts*](../secgloss/h-gly.md) (auch als [*Nachrichten Digest*](../secgloss/m-gly.md)bezeichnet) aus der Nachricht. Dieser Hashwert wird dann mit dem privaten Schlüssel des Signatur Gebers signiert. Im folgenden finden Sie eine Abbildung der Schritte, die zum Erstellen einer digitalen Signatur erforderlich sind.

![Erstellen einer digitalen Signatur aus einer Nachricht](images/capi06.png)

Zum Überprüfen einer Signatur sind sowohl die Nachricht als auch die Signatur erforderlich. Zuerst muss ein Hashwert aus der Nachricht auf die gleiche Weise erstellt werden, wie die Signatur erstellt wurde. Dieser Hashwert wird dann anhand der Signatur mit dem öffentlichen Schlüssel des Signatur Gebers überprüft. Wenn der Hashwert und die Signatur Stimmen, können Sie sicher sein, dass die Nachricht tatsächlich die Nachricht ist, die der Signatur Geber ursprünglich signiert hat, und dass Sie nicht manipuliert wurde. Das folgende Diagramm veranschaulicht den Prozess, der beim Überprüfen einer digitalen Signatur beteiligt ist.

![Überprüfen einer digitalen Signatur](images/capi07.png)

Ein Hashwert besteht aus einer kleinen Menge an Binärdaten, in der Regel um 160 Bits. Dies wird mit einem [*Hash Algorithmus*](../secgloss/h-gly.md)erzeugt. Eine Reihe dieser Algorithmen sind weiter unten in diesem Abschnitt aufgeführt.

Alle Hashwerte haben unabhängig vom verwendeten Algorithmus die folgenden Eigenschaften:

-   Die Länge des Hashwerts wird durch den verwendeten Algorithmustyp bestimmt, und seine Länge variiert nicht mit der Größe der Nachricht. Die gängigsten Hashwert-Längen sind entweder 128 oder 160 Bits.
-   Jedes Paar nicht identischer Nachrichten wird in einen vollständig anderen Hashwert übersetzt, auch wenn sich die beiden Nachrichten nur durch ein einzelnes Bit unterscheiden. Mithilfe der heutigen Technologie ist es nicht möglich, ein paar von Nachrichten zu ermitteln, die in den gleichen Hashwert übersetzt werden, ohne den Hash Algorithmus zu unterbrechen.
-   Jedes Mal, wenn eine bestimmte Nachricht mit demselben Algorithmus Hashwert verwendet wird, wird derselbe Hashwert erstellt.
-   Alle Hash Algorithmen sind unidirektional. Bei einem Hashwert ist es nicht möglich, die ursprüngliche Nachricht wiederherzustellen. Tatsächlich kann keine der Eigenschaften der ursprünglichen Nachricht mit dem Hashwert allein bestimmt werden.

 

 
