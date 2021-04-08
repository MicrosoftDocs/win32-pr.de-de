---
title: Verzeichnisdienst Funktionen (AD DS)
description: Die Verzeichnisdienst Funktionen stellen ein Dienstprogramm für die Suche eines Domänen Controllers (DC) in einer Windows NT-oder Windows 2000-Domäne bereit.
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- Verzeichnisdienst Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b071128806926e07cf61d62e53b823d8e7e1ac
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "104038447"
---
# <a name="directory-service-functions-ad-ds"></a>Verzeichnisdienst Funktionen (AD DS)

Die Verzeichnisdienst Funktionen stellen ein Dienstprogramm für die Suche eines Domänen Controllers (DC) in einer Windows NT-oder Windows 2000-Domäne bereit. Die Architektur interagiert mit Clients und Servern in allen Versionen von Windows NT und Windows 2000. Die folgenden Funktionen ermöglichen es Entwicklern, mit dem Domänen Controller und der Domänen Mitgliedschaft im Verzeichnisdienst zu arbeiten:

-   [**Dsadresssstositenames**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**Dsadresssstositenamesex**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**Dsderegisterdnshostrecords**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**Dsenum eratedomaintrusts**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**Dsgetdcclose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**Dsgetdcnext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**Dsgetdcopen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**Dsgetdcsitecoverage**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**Dsgetforesttrustinformationw**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**Dsmergeforesttrustinformationw**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**Dsrolefrememory**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**Dsvalidatesubnetname**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

Der Domänen Controller-Locator ( [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)) wird durch den Anmeldedienst implementiert. Jeder Domänen Controller registriert seinen DNS-Namen auf dem DNS-Server und seinen NetBIOS-Namen unter Verwendung eines Transport spezifischen Mechanismus, z. b. in WINS. Der Domänencontrollerlocator sucht nach dem Namen und sendet dann ein Datagramm an den DC, der den Namen registriert hat. Bei NetBIOS-Domänen Namen ist das Datagramm eine mailslotnachricht. Für DNS-Domänen Namen ist das Datagramm eine LDAP-UDP-Suche. Jeder dieser Domänen Controller antwortet, dass er zurzeit betriebsbereit ist. Der erste zu antworende DC wird an den Aufrufer zurückgegeben.

Der zurückgegebene Domänen Controller wird zwischengespeichert, sodass nachfolgende Aufrufer den vorangehenden Algorithmus nicht wiederholen und alle Aufrufer ermutigen müssen, denselben DC zu verwenden. Dadurch wird sichergestellt, dass ein einzelner Client eine konsistente Ansicht der Inhalte des DC hat.

Bei der Suche nach einem Domänen Controller anhand des DNS-Domänen namens versucht der Domänencontrollerlocator, einen DC am nächstgelegenen Standort zu finden. Jeder Domänen Controller registriert zusätzliche DNS-Einträge, die angeben, in welchem Standort sich der DC befindet und welche Standorte der DC enthält. Der Domänencontrollerlocator sucht zuerst nach diesem Website spezifischen DNS-Datensatz, bevor er nach dem DNS-Datensatz sucht, der nicht Standort spezifisch ist, wodurch ein DC an diesem Standort bevorzugt wird. Wenn der Domänencontrollerlocator ein Datagramm an den Domänen Controller sendet, sucht der Domänen Controller die IP-Adresse des Clients im Konfigurations-/Site-/Subnetzcontainer der DS nach einem Subnetzobjekt. Die **siteObject** -Eigenschaft des Subnetzobjekts definiert den Namen der Website, die den Client enthält. Der Domänen Controller antwortet auf den Ping mit dem Namen der Site, die den Client enthält, sowie auf die Angabe, ob dieser Standort von diesem Domänen Controller abgedeckt wird. Wenn der Domänen Controller diesen Standort nicht enthält und der Domänencontrollerlocator noch nicht versucht hat, einen Domänen Controller an diesem Standort zu finden, versucht der Domänencontrollerlocator erneut, einen Domänen Controller zu finden.

Um den Namen der Website zu ermitteln, die den Client enthält, verwenden Sie die Funktion [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) . Die Namen der Objekte im Konfigurations-/Site-/Subnetzcontainer müssen gültige Subnetznamen sein. Die Funktion [**dsvalidatesubnetname**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) gibt an, ob ein angegebener subnetzname gültig ist.

 

 




