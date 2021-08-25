---
description: Der Informations-DC wird verwendet, um Standardgerätedaten abzurufen.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Informationsgerätekontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974b861f47ffbd19566a5224d0c2705e9797e86abbe46005c6eb1687a9573378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779130"
---
# <a name="information-device-contexts"></a>Informationsgerätekontexte

Der Informations-DC wird verwendet, um Standardgerätedaten abzurufen. Beispielsweise kann eine Anwendung die [**CreateIC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createica) aufrufen, um einen Informations-DC für ein bestimmtes Druckermodell zu erstellen, und dann die [**GetCurrentObject-**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) und [**GetObject-Funktionen**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) aufrufen, um die Standardstift- oder Pinselattribute abzurufen. Da das System Geräteinformationen abrufen kann, ohne die Strukturen zu erstellen, die normalerweise den anderen Arten von Gerätekontexten zugeordnet sind, verursacht ein Informations-DC deutlich weniger Aufwand und wird deutlich schneller erstellt als jeder andere Typ. Nachdem eine Anwendung das Abrufen von Daten mithilfe eines Informationsdomänencontrollers abgeschlossen hat, muss sie die [**DeleteDC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) aufrufen.

 

 



