---
title: Multilink- und Rückrufverbindungen
description: Für den ersten Link in einer Multilinkverbindung legt der Authentifizierungsdienst das FLAG "RAS \_ EAP \_ FLAG FIRST \_ \_ LINK" im fFlags-Member der \_ EAP INPUT-Struktur von PPB \_ fest.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7493550863a755a87668c96dbe0ce600d524a111b7e7300b97c307f4d30c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852320"
---
# <a name="multilink-and-callback-connections"></a>Multilink- und Rückrufverbindungen

Für den ersten Link in einer Multilinkverbindung legt der Authentifizierungsdienst das FLAG "RAS \_ EAP \_ FLAG FIRST \_ \_ LINK" im **fFlags-Member** der [**\_ EAP \_ INPUT-Struktur von PPB**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) fest. Das Authentifizierungsprotokoll kann das Vorhandensein dieses Flags verwenden, um zu bestimmen, ob eine Benutzeroberfläche speziell für den ersten Link einer Multilinkverbindung vorhanden sein soll.

Wenn die Verbindung so konfiguriert ist, dass der Server den Clientcomputer zurückruft, wird das FLAG RAS \_ EAP \_ FLAG FIRST LINK für den Rückruf nicht \_ \_ festgelegt.

Wenn das Authentifizierungsprotokoll das **fSaveConnectionData-Element** von [**CSV \_ EAP \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) auf **TRUE** festlegt, erhalten nachfolgende Links in der Multilinkverbindung die neuen verbindungsspezifischen Daten. Im Fall von benutzerspezifischen Daten erhält das Authentifizierungsprotokoll jedoch weiterhin die ursprünglichen benutzerspezifischen Daten, auch wenn es das **fSaveUserData-Element** von **CSV \_ EAP \_ OUTPUT** auf **TRUE** festlegt.

Das Authentifizierungsprotokoll kann eine [interaktive Benutzeroberfläche](interactive-user-interface.md) verwenden, um Daten für einen bestimmten Link einer Multilinkverbindung zu sammeln. In diesem Fall stellt der Authentifizierungsdienst die resultierenden Daten dem Authentifizierungsprotokoll während nachfolgender Links zur Verfügung. Diese Daten werden jedoch nie im persistenten Speicher gespeichert.

 

 




