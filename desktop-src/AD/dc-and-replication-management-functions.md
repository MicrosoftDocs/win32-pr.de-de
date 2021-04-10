---
title: Domänen Controller-und Replikations Verwaltungsfunktionen
description: Dieses Thema enthält eine Liste der Funktionen, die für Domänen Controller und Replikations Verwaltung verwendet werden.
ms.assetid: a92783c2-ffb8-473e-8484-1c05ca5453ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00660658874bad4e34a8f6917e08289007cec4d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038777"
---
# <a name="domain-controller-and-replication-management-functions"></a>Domänen Controller-und Replikations Verwaltungsfunktionen

Der Domänen Controller (DC) und die Replikations Verwaltungsfunktionen stellen Tools zum Suchen von Daten zu einem Domänen Controller, zum Ändern der Namen von Netzwerk Objekten zwischen verschiedenen Formaten, zum Bearbeiten von Dienst Prinzipal Namen (SPNs) und Verzeichnisdienst-Agents (DSAs) und zum Verwalten der Replikation von Servern bereit Die folgenden Funktionen ermöglichen es Entwicklern, mit Domänen Controllern, der Replikation und dem Verzeichnisdienst zu arbeiten:

-   [**Dsaddsidhistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)
-   [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda)
-   [**Dsbindingsettimeout**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindingsettimeout)
-   [**Dsbindtoistg**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindtoistga)
-   [**Dsbindwithkred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda)
-   [**Dsbindwithspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspna)
-   [**Dsbindwithspnetx**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspnexa)
-   [**DsClientMakeSpnForTargetServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsclientmakespnfortargetservera)
-   [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa)
-   [**Dscrackspn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackspna)
-   [**Dscrackunquotedmangledrdn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackunquotedmangledrdna)
-   [**Dsfreedomaincontrollerinfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa)
-   [**Dsfreenameresult**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreenameresulta)
-   [**Dsfreepasswordanmeldeinformationen**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreepasswordcredentials)
-   [**Dsfreschemaguidmap**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa)
-   [**Dsfreespnarray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)
-   [**Dsgetdomaincontrollerinfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa)
-   [**Dsgetrdnw**](/windows/desktop/api/Dsparse/nf-dsparse-dsgetrdnw)
-   [**Dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)
-   [**Dsinverersecurityidentity**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsinheritsecurityidentitya)
-   [**Dsismangleddn**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangleddna)
-   [**Dsismangledrdnvalue**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangledrdnvaluea)
-   [**Dslistdomainsinsite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistdomainsinsitea)
-   [**Dslistinfoforserver**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistinfoforservera)
-   [**Dslistroles**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistrolesa)
-   [**Dslistserversfordomaininsite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversfordomaininsitea)
-   [**Dslistserversinsite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversinsitea)
-   [**Dslistsites**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistsitesa)
-   [**Dsmakepassword-Anmelde Informationen**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa)
-   [**Dsmakespn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna)
-   [**Dsmapschemaguids**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmapschemaguidsa)
-   [**DsQuerySitesByCost**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesbycosta)
-   [**Dsquerysitesfree**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesfree)
-   [**Dsquoterdnvalue**](/windows/desktop/api/Dsparse/nf-dsparse-dsquoterdnvaluea)
-   [**Dsremovedsdomain**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsdomaina)
-   [**Dsremovedsserver**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsservera)
-   [**Dsreplicaadd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)
-   [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck)
-   [**Dsreplicadel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)
-   [**Dsreplicafreeingefo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicafreeinfo)
-   [**Dsreplicagetinfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)
-   [**DsReplicaGetInfo2**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfo2w)
-   [**Dsreplicamodify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)
-   [**Dsreplicasync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)
-   [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla)
-   [**Dsreplicaupdaterefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)
-   [**Dsreplicaverifyobjects**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaverifyobjectsa)
-   [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)
-   [**Dsunbind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda)
-   [**Dsunquoterdnvalue**](/windows/desktop/api/Dsparse/nf-dsparse-dsunquoterdnvaluea)
-   [**Dswrite-accountspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)
-   [**Syncupdateproc**](/previous-versions/windows/desktop/legacy/ms677968(v=vs.85))

Die meisten dieser Funktionen erfordern ein Handle, das an den Verzeichnisdienst gebunden ist. Die Funktionen [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda) und [**dsbindwithkred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda) starten eine RPC-Sitzung mit einem bestimmten Domänen Controller, binden dann ein Handle an den Verzeichnisdienst und geben das Handle zurück. Wenn das Handle nicht mehr benötigt wird, verwenden Sie die [**dsunbind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda) -Funktion, um die RPC-Sitzung zu beenden und die Bindung des Handles aufzuheben.

Die Replikation erfolgt zwischen einem Quell Server und einem Zielserver. Ein Quell Server verwaltet eine Liste von Ziel Servern, auf denen er repliziert werden soll, und ein Zielserver verwaltet eine Liste der Quell Server, von denen er die Replikation empfängt. Verwenden Sie die [**dsreplicaadd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda) -Funktion, um der Liste der Quell Server auf einem Zielserver hinzuzufügen, und verwenden Sie die [**dsreplicadel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela) -Funktion, um Verweise aus der Quell Serverliste auf einem Zielserver zu entfernen. Die [**dsreplicamodify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya) -Funktion kann verwendet werden, um einen vorhandenen Quell Server Verweis auf einem Zielserver zu ändern. Um die Liste der Zielserver auf einem Quell Server zu ändern, verwenden Sie die Funktion [**dsreplicaupdaterefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa) .

Die tatsächliche Replikation wird von den Funktionen [**dsreplicasync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) und [**dsreplicasyncalldurch**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla) geführt. Die **dsreplicasync** -Funktion synchronisiert einen bestimmten Zielserver mit einem einzelnen Quell Server. Verwenden Sie die Funktion **DsReplicaSyncAll,** um einen Zielserver mit allen anderen Servern des Standorts zu synchronisieren.

 

 