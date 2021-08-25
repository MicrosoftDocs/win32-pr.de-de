---
description: Zum Senden von Daten über ein Kommunikationsmedium, z. B. eine Telefonleitung, müssen die Daten&8212 serialisiert werden. Das heißt, sie müssen in eine Zeichenfolge von Einsen und Nullen konvertiert werden, die seriell über die Linie übertragen \# werden.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Codierte und decodierte Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063f18a4f58f2989e2bd0b890fd11a7ab6022a3de255385b1cf529afb5493485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874945"
---
# <a name="encoded-and-decoded-data"></a>Codierte und decodierte Daten

To send data over a communication medium such as a phone line, the data must be [*serialized*](../secgloss/s-gly.md)— that is, converted into a string of ones and zeros that are transmitted serially over the line. Die Serialisierung muss so erfolgen, dass der Computer, der die Daten empfängt, die Daten wieder in das ursprüngliche Format konvertieren kann. Die Serialisierung wird als Kommunikationsprotokoll [*bezeichnet*](../secgloss/c-gly.md)und wird sowohl von Software als auch von Datenübertragungshardware gesteuert. Es gibt mehrere Ebenen, auf denen die Daten konvertiert werden. Die folgende Abbildung zeigt eine deutlich vereinfachte Ansicht der Kommunikationsprotokollebenen.

![Kommunikationsprotokollebenen](images/layer.png)

Die obige Abbildung zeigt die Anwendungsschicht auf Computer 1, die die zu übertragenden Daten (die in der Regel aus einer Kombination aus Textzeichen und Zahlen bestehen) an die \# Codierungs-/Decodierungsebene sendet. Die Codierungs-/Decodierungsebene codiert die Daten in einen Datenstrom von Computerbytes. Auf der untersten Ebene, der Hardwareschicht, konvertiert die Hardware die Datenbytes in einen seriellen Datenstrom von Einsen und Nullen, der über die Zeile an Computer \# 2 übertragen wird. Die Hardwareschicht von Computer 2 konvertiert die Einsen und Nullen zurück in Computerbytes und übergibt sie zur Decodierung an die \# Codierungs-/Decodierungsebene. Die Codierungs-/Decodierungsebene decodiert die Bytes wieder in ihr ursprüngliches Format und übergibt die Daten an die Anwendungsschicht.

An accepted software design principle is to use *abstraction*, that is, the process of describing a problem or object in terms of its general parameters rather than describing all the details necessary to solve the problem, or describing all the details of an object. Mithilfe der Abstraktion kann ein Designer ein Softwareobjekt mit bestimmten Qualitäten angeben, ohne bedenken zu müssen, wie das Objekt tatsächlich im Softwarecode implementiert wird. Eine solche Vorgehensweise lässt die Implementierung geöffnet. Außerdem vereinfacht es die Spezifikation und ermöglicht es, Axiome über das Objekt zu geben, die bei der Objekt implementiert werden können. Diese Axiomen können dann angenommen werden, wenn das Objekt in einem anderen Objekt höherer Ebene verwendet wird. Abstraktion ist das Kennzeichen der meisten sten Softwarespezifikationen.

Die [*meisten Kommunikationsprotokolle*](../secgloss/c-gly.md) umfassen eine große Abstraktion. Objekte auf höheren Ebenen werden abstrakt definiert und sollen mithilfe von Objekten auf niedrigeren Ebenen implementiert werden. Beispielsweise kann für einen Dienst auf einer Ebene die Übertragung bestimmter abstrakter Objekte zwischen Computern erforderlich sein. Eine niedrigere Ebene kann Codierungsregeln verwenden, um die abstrakten Objekte in Zeichenfolgen von Einsen und Nullen zu transformieren.

Eine gängige Methode zum Angeben abstrakter Objekte, die seriell übertragen werden sollen, heißt [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1). ASN.1 ist in der CCITT-Empfehlung [*X.208 definiert.*](../secgloss/x-gly.md) Ein Satz von ASN.1-Regeln zum Darstellen solcher Objekte als Zeichenfolgen von Einsen und Nullen wird [*als Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) bezeichnet und in CCITT Recommendation [*X.509*](../secgloss/x-gly.md), Section 8.7 definiert. Dies sind die Codierungsmethoden, die derzeit von CryptoAPI verwendet werden.

Weitere Informationen zu Codierungs-/Decodierungsfunktionen finden Sie unter [Objektcodierungs- und Decodierungsfunktionen.](cryptography-functions.md)

 

 
