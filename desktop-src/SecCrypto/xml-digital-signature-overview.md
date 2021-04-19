---
description: XML ist ein Industriestandard, mit dem strukturierte Daten beschrieben werden. Eine digitale XML-Signatur ist eine XML-Darstellung einer digitalen Signatur, die die Möglichkeit bietet, den Ursprung und die Integrität von XML-Dokumenten und extern referenzierten Daten zu überprüfen.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Übersicht über die digitale XML-Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367973"
---
# <a name="xml-digital-signature-overview"></a>Übersicht über die digitale XML-Signatur

XML ist ein Industriestandard, mit dem strukturierte Daten beschrieben werden. Eine digitale XML-Signatur ist eine XML-Darstellung einer [*digitalen Signatur*](../secgloss/d-gly.md) , die die Möglichkeit bietet, den Ursprung und die Integrität von XML-Dokumenten und extern referenzierten Daten zu überprüfen. Digitale XML-Signaturen können verwendet werden, um beliebige Daten zu signieren, einschließlich XML-Dokument oder-Fragment, HTML-Seite, nur-Text oder binär codierte Daten, z. b. eine JPEG-Datei.

Das von der kryptotxml Digital Signature-API unterstützte XML-Format der digitalen Signatur wird durch die W3C-Empfehlung XML-Signatur Syntax und-Verarbeitung (Second Edition) angegeben.

Die digitale Signatur von cryptxml implementiert die Unterstützung für die erforderlichen Signatur Typen, Kryptografiealgorithmen, Kanonisierungsalgorithmen und die angegebene eingeschlossene Transformation.

Entwickler können den von cryptxml unterstützten Standardsatz von Kryptografiealgorithmen durch Erstellen von kryptografieerweiterungs-DLLs erweitern. Entwickler können auch Ihre eigenen benutzerdefinierten Transformationen und Kanonisierungsalgorithmen zusätzlich zur cryptxml-API erstellen. Entwickler können die cryptxml-APIs mit den Windows-Zertifikat-APIs verwenden.

 

 
