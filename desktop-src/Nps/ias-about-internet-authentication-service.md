---
title: Informationen zu NPS-Erweiterungen
description: In diesem Abschnitt wird beschrieben, wie DLLs implementiert werden, um die Funktionalität von NPS zu erweitern. Es beschreibt die Interaktion zwischen NPS und den DLLs und zeigt einige Entwurfs Überlegungen hinsichtlich der DLLs an.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339898"
---
# <a name="about-nps-extensions"></a>Informationen zu NPS-Erweiterungen

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

In diesem Abschnitt wird beschrieben, wie DLLs implementiert werden, um die Funktionalität von NPS zu erweitern. Es beschreibt die Interaktion zwischen NPS und den DLLs und zeigt einige Entwurfs Überlegungen hinsichtlich der DLLs an.

NPS bietet zwei Erweiterungs Punkte, eine für die Authentifizierung und die andere für die Autorisierung. Authentifizierung bezieht sich auf die Überprüfung der Identität des Benutzers. Autorisierung bezieht sich auf die Bestimmung der Dienste, die das Netzwerk für den Benutzer bereitstellen soll. Die beiden Erweiterungs Punkte entsprechen authentifizierungserweiterungs-DLLs und DLLs für Autorisierungs Erweiterungen. Jeder Erweiterungs Punkt kann mehrere DLLs unterstützen.

NPS bietet Authentifizierungs-und Autorisierungs Dienste. Authentifizierungserweiterungs-DLLs werden von NPS vor der integrierten NPS-Authentifizierung und-Autorisierung aufgerufen. Autorisierungs Erweiterungs-DLLs werden nach der NPS-Authentifizierung und-Autorisierung aufgerufen.

Das folgende Diagramm veranschaulicht den Fluss von Paketen über einen NPS-RADIUS-Server, der mithilfe von Erweiterungs-DLLs erweitert wird.

![NPS-Authentifizierungs-und-Autorisierungs Prozess](images/ias03.png)

Wenn eine authentifizierungserweiterungs-dll "Accept" zurückgibt, überspringt das Paket die NPS-Authentifizierung und wechselt direkt zur NPS-Autorisierung.

> [!Note]  
> Wenn mehrere authentifizierungserweiterungs-DLLs vorhanden sind, können die restlichen Erweiterungs-DLLs ebenfalls übersprungen werden. Weitere Informationen finden [Sie unter Einrichten der Erweiterungs-DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .

 

Wenn eine Authentifizierungs Erweiterungs-DLL "Continue" zurückgibt, wird das Paket an die NPS-Authentifizierung und dann an die NPS-Autorisierung geleitet.

> [!Note]  
> Wenn mehrere authentifizierungserweiterungs-DLLs vorhanden sind, werden die restlichen authentifizierungserweiterungs-DLLs vor der NPS-Authentifizierung aufgerufen.

 

In den folgenden Themen werden die Erweiterungs-DLLs ausführlicher beschrieben:

-   [Einrichten der Erweiterungs-DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Aufrufen der Erweiterungs-DLLs](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Benutzer Identifizierungs Attribute](/windows/desktop/Nps/ias-user-identification-attributes)

 

 