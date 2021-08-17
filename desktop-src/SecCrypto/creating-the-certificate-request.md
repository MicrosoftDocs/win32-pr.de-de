---
description: Der Prozess zum Erstellen einer Zertifikatanforderung umfasst das Sammeln bestimmter Informationen vom Anfordernden.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Erstellen der Zertifikatanforderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607ebbfd5d230c216c2b7ebc4d3b217e1f8c0d2a375d39cdd6b311ec145be361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768880"
---
# <a name="creating-the-certificate-request"></a>Erstellen der Zertifikatanforderung

Der Prozess zum Erstellen einer Zertifikatanforderung umfasst das Sammeln bestimmter Informationen vom Anfordernden. In der Regel erfolgt dies über eine Art benutzeroberfläche (UI), obwohl die Informationen direkt aus einer Datenbank übernommen werden können, ohne dass eine Benutzeroberfläche benötigt wird. Die erforderliche Informationsebene wird durch die Richtlinie der [*Zertifizierungsstelle*](../secgloss/c-gly.md) festgelegt.

Ein Beispiel für die erforderlichen Informationen könnte wie folgt lauten:

-   Allgemeiner Name
-   Komponentenname
-   Name des Unternehmens
-   City
-   State
-   Land/Region

> [!Note]  
> Die -Schnittstelle ist so konzipiert, dass eine einzelne Anforderung für jede xenroll-Instanz gestellt wird. Es muss eine separate xenroll-Instanz erstellt werden, um jede [*Zertifikatanforderung zu erstellen.*](../secgloss/c-gly.md)

 

Informationen zur Verwendung der Zertifikatregistrierungssteuerung zum Anfordern eines Zertifikats in bestimmten Programmiersprachen finden Sie in den folgenden Themen:

-   [Anforderungsbeispiel in C++](request-sample-in-c-.md)
-   [Anforderungsbeispiel in VBScript](request-sample-in-vbscript.md)

 

 
