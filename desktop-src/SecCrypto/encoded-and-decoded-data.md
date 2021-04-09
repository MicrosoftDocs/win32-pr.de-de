---
description: Um Daten über ein Kommunikationsmedium (z. b. eine Telefonleitung) zu senden, müssen die Daten&8212 serialisiert werden, d \# . h., Sie werden in eine Zeichenfolge von einer und Nullen konvertiert, die Seriell über die Zeile übertragen werden.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Codierte und decodierte Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b130232ac67503c6a20835c4c9b4e728b36f8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958836"
---
# <a name="encoded-and-decoded-data"></a>Codierte und decodierte Daten

Zum Senden von Daten über ein Kommunikationsmedium, z. b. eine Telefonleitung, müssen die Daten [*serialisiert*](../secgloss/s-gly.md)werden – d. h., Sie werden in eine Zeichenfolge von einem und Nullen konvertiert, die Seriell über die Zeile übertragen werden. Die Serialisierung muss so durchgeführt werden, dass der Computer, der die Daten empfängt, die Daten wieder in das ursprüngliche Format konvertieren kann. Die Art und Weise, wie die Serialisierung erreicht wird, wird als [*Kommunikationsprotokoll*](../secgloss/c-gly.md)bezeichnet und sowohl von der Software als auch von der Datenübertragungs Hardware gesteuert. Es gibt mehrere Ebenen, auf denen die Daten konvertiert werden. In der folgenden Abbildung ist eine stark vereinfachte Ansicht der Kommunikationsprotokoll Ebenen dargestellt.

![Kommunikationsprotokoll Ebenen](images/layer.png)

Die obige Abbildung zeigt die Anwendungsschicht auf Computer \# 1, die die zu übertragenden Daten (die normalerweise aus einer Kombination aus Textzeichen und Ziffern besteht) mit der Codieren/Decodieren-Schicht sendet. Die Codieren/Decodieren-Ebene codiert die Daten in einen Stream von Computer bytes. Auf der niedrigsten Ebene, der Hardware Schicht, konvertiert die Hardware die Bytes der Daten in einen seriellen Datenstrom von einem und Nullen, die über die Zeile an Computer 2 übertragen werden \# . Die Hardwareebene von Computer \# 2 konvertiert die Werte und Nullen zurück in Computer Bytes und übergibt sie zur Decodierung an die Codierungs Schicht. Die Codieren/Decodieren-Ebene decodiert die Bytes zurück in Ihr ursprüngliches Format und übergibt die Daten an die Anwendungsschicht.

Ein akzeptiertes Software Entwurfs Prinzip ist die Verwendung von *Abstraktion*, d. h. das Beschreiben eines Problems oder Objekts in Bezug auf die allgemeinen Parameter, anstatt alle Details zu beschreiben, die zum Beheben des Problems erforderlich sind, oder alle Details eines Objekts zu beschreiben. Mithilfe der Abstraktion kann ein Designer ein Software Objekt angeben, das über bestimmte Qualitäten verfügt, ohne dass es darum geht, wie das Objekt tatsächlich im Software Code implementiert wird. Bei einer solchen Vorgehensweise bleibt die Implementierung geöffnet. Außerdem vereinfacht Sie die Spezifikation und ermöglicht das State von Axioms über das Objekt, das bei der Implementierung des Objekts nachgewiesen werden kann. Diese Axioms kann dann angenommen werden, wenn das Objekt in einem anderen Objekt der höheren Ebene verwendet wird. Abstraktion ist das Merkmal der meisten modernen Software Spezifikationen.

Die meisten [*Kommunikationsprotokolle*](../secgloss/c-gly.md) beinhalten eine gute Abstraktion. Objekte auf höheren Ebenen werden abstrakter definiert und sind für die Implementierung mithilfe von Objekten auf niedrigeren Ebenen vorgesehen. Beispielsweise erfordert ein Dienst auf einer Ebene möglicherweise das übertragen bestimmter abstrakter Objekte zwischen Computern. Eine Ebene auf niedrigerer Ebene kann Codierungsregeln verwenden, um die abstrakten Objekte in Zeichen folgen von einem und Nullen umzuwandeln.

Eine gängige Methode zum angeben abstrakter Objekte, die seriell übertragen werden sollen, wird als [*abstrakte Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1) bezeichnet. ASN. 1 ist in der CCITT-Empfehlung [*X. 208*](../secgloss/x-gly.md)definiert. Ein Satz von ASN. 1-Regeln für das darstellen von Objekten als Zeichen folgen und Nullen wird als [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) bezeichnet und wird in der CCITT-Empfehlung [*X. 509*](../secgloss/x-gly.md), Abschnitt 8,7, definiert. Dies sind die Codierungs Methoden, die derzeit von CryptoAPI verwendet werden.

Weitere Informationen zum Codieren/Decodieren von Funktionen finden Sie unter [objektcodierungs-und Decodierungs Funktionen](cryptography-functions.md).

 

 
