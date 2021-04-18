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
# <a name="multilink-and-callback-connections"></a><span data-ttu-id="222fd-103">Multilink-und Rückruf Verbindungen</span><span class="sxs-lookup"><span data-stu-id="222fd-103">Multilink and Callback Connections</span></span>

<span data-ttu-id="222fd-104">Für den ersten Link in einer Verbindung mit mehreren Links legt der Authentifizierungsdienst das Flag für das erste Flag für RAS- \_ EAP \_ \_ \_ im **fFlags** -Member der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="222fd-104">For the first link in a multilink connection, the authentication service sets the RAS\_EAP\_FLAG\_FIRST\_LINK flag in the **fFlags** member of the [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) structure.</span></span> <span data-ttu-id="222fd-105">Das Authentifizierungsprotokoll kann das vorhanden sein dieses Flags verwenden, um zu bestimmen, ob eine Benutzeroberfläche speziell für den ersten Link einer Multilinkverbindung vorhanden sein soll.</span><span class="sxs-lookup"><span data-stu-id="222fd-105">The authentication protocol can use the presence of this flag to determine whether to present a user interface specifically for the first link of a multilink connection.</span></span>

<span data-ttu-id="222fd-106">Wenn die Verbindung so konfiguriert ist, dass der Server den Client Computer zurückruft, wird das RAS-Flag \_ für das EAP- \_ Flag \_ erste \_ Links nicht für den Rückruf festgelegt.</span><span class="sxs-lookup"><span data-stu-id="222fd-106">If the connection is configured so that the server calls back the client computer, the RAS\_EAP\_FLAG\_FIRST\_LINK flag will not be set on the callback.</span></span>

<span data-ttu-id="222fd-107">Wenn das Authentifizierungsprotokoll den **fsaveconnectiondata** -Member der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) auf **true** festlegt, werden nachfolgende Links in der mehrfach-Verbindung die neuen Verbindungs spezifischen Daten empfangen.</span><span class="sxs-lookup"><span data-stu-id="222fd-107">If the authentication protocol sets the **fSaveConnectionData** member of [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) to **TRUE**, subsequent links in the multilink connection receive the new connection-specific data.</span></span> <span data-ttu-id="222fd-108">Im Fall von benutzerspezifischen Daten erhält das Authentifizierungsprotokoll jedoch weiterhin die ursprünglichen benutzerspezifischen Daten, auch wenn der **fsaveuserdata** -Member der **PPP- \_ EAP- \_ Ausgabe** auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="222fd-108">In the case of user-specific data, however, the authentication protocol continues to get the original user-specific data even if it sets the **fSaveUserData** member of **PPP\_EAP\_OUTPUT** to **TRUE**.</span></span>

<span data-ttu-id="222fd-109">Das Authentifizierungsprotokoll kann eine [interaktive Benutzeroberfläche](interactive-user-interface.md) verwenden, um Daten für einen bestimmten Link einer Multilinkverbindung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="222fd-109">The authentication protocol may use an [interactive user interface](interactive-user-interface.md) to collect data for a particular link of a multilink connection.</span></span> <span data-ttu-id="222fd-110">In diesem Fall stellt der Authentifizierungsdienst die resultierenden Daten für das Authentifizierungsprotokoll bei nachfolgenden Links zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="222fd-110">In this case, the authentication service makes the resulting data available to the authentication protocol during subsequent links.</span></span> <span data-ttu-id="222fd-111">Diese Daten werden jedoch nie im permanenten Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="222fd-111">However, this data is never saved to persistent storage.</span></span>

 

 




