---
description: Personen in meiner Umgebung Stores
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Personen in meiner Umgebung Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945a49d174f53037427aaa2f45dc0f567dc0acdba57e4a0b0231954e7e66fe90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061378"
---
# <a name="people-near-me-stores"></a>Personen in meiner Umgebung Stores

Anwendungen, die [Personen in meiner Umgebung](about-people-near-me.md) (PNM) verwenden können, können die folgenden Datenspeicher verwenden:

### <a name="windows-address-book"></a>Windows Adressbuch

Der Windows Adressbuch speichert Informationen zu Kontakten und ihren digitalen Zertifikaten. Der Kontakt **"Me",** der den derzeit angemeldeten Benutzer darstellt, wird ebenfalls im Windows Adressbuch gespeichert.

### <a name="certificate-store"></a>Zertifikatspeicher

Das Zertifikat Store enthält das selbstsignte Zertifikat für den Kontakt **"Me".**

### <a name="application-store"></a>Anwendungsstore

Ein Anwendungsinstallationsprogramm registriert eine Anwendung während des Installationsvorgangs bei PNM. Dies sind die Objekte, nach denen andere Benutzer suchen können, wenn sie versuchen, eine Verbindung mit einem Benutzer mit einer gängigen Anwendung wie einem Computerspiel herzustellen. Die Anwendungs-Store enthält für jede Anwendung den Namen der Anwendung, eine GUID (Globally Unique Identifier), einen Bereich der Anwendung, eine Beschreibung und einen Pfad zur ausführbaren Datei des Programms. Der Bereich einer Anwendung kann auf Keine (nicht angekündigt), Personen in meiner Umgebung (im lokalen Subnetz angekündigt), Kontakte (nur für Kontakte angekündigt) oder Alle (im lokalen Subnetz und für Kontakte angekündigt) festgelegt werden. Die Application Store befindet sich in der Registrierung Windows Vista.

 

 



