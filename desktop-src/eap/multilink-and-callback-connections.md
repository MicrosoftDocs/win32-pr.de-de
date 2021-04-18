---
title: Multilink-und Rückruf Verbindungen
description: Für den ersten Link in einer Verbindung mit mehreren Links legt der Authentifizierungsdienst das Flag für das erste Flag für RAS- \_ EAP \_ \_ \_ im fFlags-Member der PPP- \_ EAP- \_ Eingabe Struktur fest.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106340879"
---
# <a name="multilink-and-callback-connections"></a>Multilink-und Rückruf Verbindungen

Für den ersten Link in einer Verbindung mit mehreren Links legt der Authentifizierungsdienst das Flag für das erste Flag für RAS- \_ EAP \_ \_ \_ im **fFlags** -Member der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur fest. Das Authentifizierungsprotokoll kann das vorhanden sein dieses Flags verwenden, um zu bestimmen, ob eine Benutzeroberfläche speziell für den ersten Link einer Multilinkverbindung vorhanden sein soll.

Wenn die Verbindung so konfiguriert ist, dass der Server den Client Computer zurückruft, wird das RAS-Flag \_ für das EAP- \_ Flag \_ erste \_ Links nicht für den Rückruf festgelegt.

Wenn das Authentifizierungsprotokoll den **fsaveconnectiondata** -Member der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) auf **true** festlegt, werden nachfolgende Links in der mehrfach-Verbindung die neuen Verbindungs spezifischen Daten empfangen. Im Fall von benutzerspezifischen Daten erhält das Authentifizierungsprotokoll jedoch weiterhin die ursprünglichen benutzerspezifischen Daten, auch wenn der **fsaveuserdata** -Member der **PPP- \_ EAP- \_ Ausgabe** auf **true** festgelegt ist.

Das Authentifizierungsprotokoll kann eine [interaktive Benutzeroberfläche](interactive-user-interface.md) verwenden, um Daten für einen bestimmten Link einer Multilinkverbindung zu erfassen. In diesem Fall stellt der Authentifizierungsdienst die resultierenden Daten für das Authentifizierungsprotokoll bei nachfolgenden Links zur Verfügung. Diese Daten werden jedoch nie im permanenten Speicher gespeichert.

 

 




