---
title: Konfigurieren der EAP-Methode Benutzeroberfläche
description: Erläutert, wie sie durch Bereitstellen einer EAP-Methodenkonfiguration für EAPHost konfiguriert wird.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6709e68bf20d8f38d3685f66e45313083e70e46b1a8a0bb0675616bdb4e8bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086704"
---
# <a name="configuring-the-eap-method-user-interface"></a>Konfigurieren der EAP-Methode Benutzeroberfläche

In diesem Thema wird erläutert, wie sie durch Bereitstellen einer EAP-Methodenkonfiguration für EAPHost konfiguriert wird.

Damit eine Unterstützung eine EAP-basierte Authentifizierung mithilfe von EAPHost durchführen kann, muss eine Unterstützung EAPHost über die [**EapHostPeerBeginSession-Funktion**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) eine EAP-Methodenkonfiguration bereitstellen.

1.  Um die Konfiguration der EAP-Methode zu erhalten, fragt eine Unterstützung in der Regel EAPHost mithilfe von [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) ab, um den vollständigen Satz von EAP-Methoden zu erlernen, die auf dem lokalen Computer verfügbar und installiert sind. Die Liste der Methoden wird dem Benutzer in der Regel in einem Kombinationsfeld oder einem anderen Benutzeroberflächensteuerelement angezeigt, mit dem der Benutzer die gewünschte Methode auswählen kann.
    > [!Note]  
    > Die Unterstützung kann die angezeigte Liste von Methoden basierend auf den Methodeneigenschaftsbits filtern, die in **EAP \_ METHOD \_ INFO.eapProperties** angegeben sind. Einige Methoden sind möglicherweise nicht für die Sicherheitsmerkmale des Transports geeignet, der von der Suppliplizierung bereitgestellt wird, z. B. .

     

2.  Sobald das Ui-Steuerelement mit den möglichen EAP-Methoden aufgefüllt wurde, wählt der Benutzer die Methode aus, die er konfigurieren möchte. In der Regel stellt die -Unterstützung eine **Konfigurations-** oder **Eigenschaftenschaltfläche** für den Benutzer bereit, um auf die Konfigurationseigenschaften der ausgewählten EAP-Methode zuzugreifen.
    > [!Note]
    > Die Unterstützung ist sich bewusst, dass es benutzerkonfigurierbare Eigenschaften gibt, die auf dem **eapPropSupportsConfig-Bit** basieren, das in **EAP \_ METHOD \_ INFO.eapProperties** aktiviert wird.
    >
    > Weitere Informationen finden Sie unter [**EAP-Methodeneigenschaften.**](eap-method-properties.md)

     

3.  Wenn der Benutzer auf das entsprechende UI-Steuerelement klickt, ruft die Supplizierung [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)auf und übergibt an die Funktion den **HWND-Wert** für die eigene Benutzeroberfläche, die [**\_ EAP-METHODENTYP-Struktur, \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) die aus der Abfrage an die [**\_ EAP-METHODEN-INFO-Struktur \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) abgerufen wurde, und andere erforderliche Parameter.
4.  Durch aufrufen von [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) wird die eigene Konfigurationsbenutzeroberfläche einer EAP-Methode aufgerufen. Bei rückgabe von **EapHostPeerInvokeConfigUI** gibt die Funktion ein EAP-Methodenkonfigurations-BLOB als Out-Parameter zurück.
5.  Die -Unterstützung speichert das Konfigurations-BLOB zusammen mit der [**\_ EAP-METHODENTYP-Struktur \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) für die Verwendung mit [**EapHostPeerBeginSession.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
6.  Die genaue Methode zum Speichern des konfigurierbaren BLOB liegt vollständig bei der Unterstützung. Die Unterstützung sollte die Konfiguration jedoch immer in einer geeigneten, sicheren Weise speichern, die den Konfigurationsdaten der System- und Benutzerauthentifizierung entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Übertragen von Daten zwischen suppliplipli und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplikationen](eaphost-supplicants.md)
</dt> </dl>

 

 




