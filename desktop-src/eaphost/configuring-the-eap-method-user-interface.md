---
title: Konfigurieren der Benutzeroberfläche der EAP-Methode
description: Erläutert das Konfigurieren des Supplicant durch Bereitstellen einer EAP-Methoden Konfiguration für EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106341907"
---
# <a name="configuring-the-eap-method-user-interface"></a>Konfigurieren der Benutzeroberfläche der EAP-Methode

In diesem Thema wird erläutert, wie Sie den Supplicant konfigurieren, indem Sie EAPHost eine EAP-Methoden Konfiguration bereitstellen.

Damit ein Supplicant eine EAP-basierte Authentifizierung mithilfe von EAPHost ausführen kann, muss ein Supplicant eine EAP-Methoden Konfiguration für EAPHost über die [**eaphostpeerbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) -Funktion bereitstellen.

1.  Um die EAP-Methoden Konfiguration zu erhalten, fragt ein Supplicant in der Regel EAPHost mithilfe von [**eaphostpeergetmethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) ab, um den gesamten Satz von EAP-Methoden zu erlernen, die auf dem lokalen Computer verfügbar und installiert sind. Die Liste der Methoden wird dem Benutzer in der Regel in einem Kombinations Feld oder einem anderen UI-Steuerelement angezeigt, das es dem Benutzer ermöglicht, die gewünschte Methode auszuwählen.
    > [!Note]  
    > Der Supplicant kann die angezeigte Liste der Methoden basierend auf den in der **EAP-Methoden \_ \_ Info. eapproperties** angezeigten Methoden Eigenschaften Bits filtern. Einige Methoden sind möglicherweise nicht für die Sicherheitsmerkmale des vom Supplicant bereitgestellten Transports geeignet.

     

2.  Sobald das UI-Steuerelement mit dem Satz möglicher EAP-Methoden aufgefüllt ist, wählt der Benutzer die Methode aus, die Sie konfigurieren möchten. In der Regel stellt der Supplicant eine **Konfigurations** -oder **Eigenschaften** Schaltfläche bereit, damit der Benutzer auf die Konfigurations Eigenschaften der ausgewählten EAP-Methode zugreifen kann.
    > [!Note]
    > Der Supplicant weiß, dass es vom benutzerkonfigurierbare Eigenschaften gibt, die auf dem in den **EAP-Methoden Info (EAP- \_ Methoden \_ Info**) aktivierten **eappropsupportsconfig** -Bit basieren.
    >
    > Weitere Informationen finden Sie unter [**Eigenschaften der EAP-Methode**](eap-method-properties.md).

     

3.  Wenn der Benutzer auf das entsprechende UI-Steuerelement klickt, ruft der Supplicant [**eaphostpeerinvokeconfigui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)auf und übergibt an die Funktion den **HWND** -Wert für die eigene Benutzeroberfläche des Supplicant, die [**EAP- \_ \_ Methodentyp**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) Struktur, die von der Abfrage an die [**EAP- \_ Methoden \_ Informations**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) Struktur und andere erforderliche Parameter abgerufen wird.
4.  Durch Aufrufen von [**eaphostpeerinvokeconfigui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) wird die eigene Konfigurations Benutzeroberfläche einer EAP-Methode aufgerufen. Bei der Rückgabe von **eaphostpeerinvokeconfigui** gibt die Funktion ein EAP-methodenkonfigurationsblob als out-Parameter zurück.
5.  Der Supplicant speichert das konfigurationsblob zusammen mit der [**EAP \_ - \_ Methodentyp**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) Struktur zur Verwendung mit [**eaphostpeerbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).
6.  Die genaue Methode zum Speichern des Konfiguration für-BLOBs ist vollständig auf dem Supplicant. Der Supplicant sollte die Konfiguration jedoch immer auf geeignete, sichere Weise speichern, die für Konfigurationsdaten der System-und Benutzerauthentifizierung geeignet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren In-Band NAP-Unterstützung für EAP-Methoden](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Übertragen von Daten zwischen den Supplicant-und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




