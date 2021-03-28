---
description: Mithilfe der Information DC werden Standardgeräte Daten abgerufen.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Informationsgeräte Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528325"
---
# <a name="information-device-contexts"></a>Informationsgeräte Kontexte

Mithilfe der Information DC werden Standardgeräte Daten abgerufen. Eine Anwendung kann z. b. die Funktion " [**deeic**](/windows/desktop/api/Wingdi/nf-wingdi-createica) " aufrufen, um einen Informations-DC für ein bestimmtes Drucker Modell zu erstellen, und dann die Funktionen " [**getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) " und " [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) " aufrufen, um die Standard Stift-oder Pinsel Attribute abzurufen. Da das Systemgeräte Informationen abrufen kann, ohne die Strukturen zu erstellen, die normalerweise mit den anderen Typen von Geräte Kontexten verknüpft sind, umfasst ein Informations-DC weitaus weniger Aufwand und wird erheblich schneller erstellt als jeder andere Typ. Nachdem eine Anwendung das Abrufen von Daten mithilfe eines Informations-DC abgeschlossen hat, muss Sie die [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) -Funktion aufrufen.

 

 



