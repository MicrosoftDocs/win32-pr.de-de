---
description: Beim Erstellen einer Zertifikat Anforderung werden bestimmte Informationen von der anfordernden Person gesammelt.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Erstellen der Zertifikat Anforderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347137"
---
# <a name="creating-the-certificate-request"></a>Erstellen der Zertifikat Anforderung

Beim Erstellen einer Zertifikat Anforderung werden bestimmte Informationen von der anfordernden Person gesammelt. Dies erfolgt in der Regel über eine Art von Benutzeroberfläche (User Interface, UI), obwohl die Informationen direkt aus einer Datenbank abgerufen werden können, ohne dass eine Benutzeroberfläche erforderlich ist. Die erforderliche Ebene der Informationen wird durch die Richtlinie der Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) festgelegt.

Ein Beispiel für die erforderlichen Informationen könnte wie folgt lauten:

-   Allgemeiner Name
-   Einheits Name
-   Name des Unternehmens
-   City
-   State
-   Land/Region

> [!Note]  
> Die-Schnittstelle ist so konzipiert, dass für jede Xenroll-Instanz eine einzelne Anforderung ausgeführt wird. Eine separate Xenroll-Instanz muss erstellt werden, um jede [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu erstellen.

 

Informationen zur Verwendung der Zertifikat Registrierungs Steuerung zum Anfordern eines Zertifikats in bestimmten Programmiersprachen finden Sie in den folgenden Themen:

-   [Anforderungs Beispiel in C++](request-sample-in-c-.md)
-   [Anforderungs Beispiel in VBScript](request-sample-in-vbscript.md)

 

 
