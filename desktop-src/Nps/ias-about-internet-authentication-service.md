---
title: Informationen zu NPS-Erweiterungen
description: In diesem Abschnitt wird beschrieben, wie DLLs implementiert werden, um die Funktionalität von NPS zu erweitern. Es beschreibt die Interaktion zwischen NPS und den DLLs und stellt einige Entwurfsüberlegungen zu den DLLs vor.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204fff8d97548e79eed3e317b3e14291e7288b55c51384c25ef8b912ad2d6095
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799464"
---
# <a name="about-nps-extensions"></a>Informationen zu NPS-Erweiterungen

> [!Note]  
> Internet Authentication Service (IAS) wurde ab Windows Server 2008 in Network Policy Server (NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

In diesem Abschnitt wird beschrieben, wie DLLs implementiert werden, um die Funktionalität von NPS zu erweitern. Es beschreibt die Interaktion zwischen NPS und den DLLs und stellt einige Entwurfsüberlegungen zu den DLLs vor.

NPS bietet zwei Erweiterungspunkte, einen für die Authentifizierung und den anderen für die Autorisierung. Authentifizierung bezieht sich auf die Überprüfung der Identität des Benutzers. Autorisierung bezieht sich darauf, zu bestimmen, welche Dienste das Netzwerk für den Benutzer bereitstellen soll. Die beiden Erweiterungspunkte entsprechen Authentifizierungserweiterungs-DLLs und Autorisierungserweiterungs-DLLs. Jeder Erweiterungspunkt kann mehrere DLLs unterstützen.

NPS stellt sowohl Authentifizierungs- als auch Autorisierungsdienste zur Verfügung. Authentifizierungserweiterungs-DLLs werden von NPS vor der integrierten NPS-Authentifizierung und -Autorisierung aufgerufen. Autorisierungserweiterungs-DLLs werden nach der NPS-Authentifizierung und -Autorisierung aufgerufen.

Das folgende Diagramm veranschaulicht den Fluss von Paketen über einen NPS-RADIUS-Server, der mithilfe von Erweiterungs-DLLs erweitert wird.

![nps-Authentifizierungs- und -Autorisierungsprozess](images/ias03.png)

Wenn eine Authentifizierungserweiterungs-DLL ACCEPT zurückgibt, überspringt das Paket die NPS-Authentifizierung und geht direkt zur NPS-Autorisierung über.

> [!Note]  
> Wenn mehrere Authentifizierungserweiterungs-DLLs vorhanden sind, können auch die restlichen Erweiterungs-DLLs übersprungen werden. Weitere [Informationen finden Sie unter Einrichten der Erweiterungs-DLLs.](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)

 

Wenn eine Authentifizierungserweiterungs-DLL CONTINUE zurückgibt, wird das Paket an die NPS-Authentifizierung und dann an die NPS-Autorisierung gesendet.

> [!Note]  
> Wenn mehrere Authentifizierungserweiterungs-DLLs vorhanden sind, werden die restlichen Authentifizierungserweiterungs-DLLs vor der NPS-Authentifizierung aufgerufen.

 

In den folgenden Themen werden die Erweiterungs-DLLs ausführlicher beschrieben:

-   [Einrichten der Erweiterungs-DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Aufrufen der Erweiterungs-DLLs](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Benutzeridentifikationsattribute](/windows/desktop/Nps/ias-user-identification-attributes)

 

 