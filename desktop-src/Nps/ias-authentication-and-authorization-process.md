---
title: Aufrufen der Erweiterungs-DLLs
description: Diese Funktion wird für jedes gültige Authentifizierungs-oder Buchhaltungs Paket aufgerufen, das vom Netzwerk Zugriffs Server (NAS) empfangen wird.
ms.assetid: 6d738ad7-cce5-4835-97d6-c57173c79a16
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc96fab078a982f23f5f5dd86d51dbed46d5541
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948970"
---
# <a name="invoking-the-extension-dlls"></a>Aufrufen der Erweiterungs-DLLs

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

NPS-Erweiterungs-DLLs müssen mindestens eine der folgenden Rückruf Funktionen exportieren: [*radiusextensionprocess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process), [*radiusextensionprocessex*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)oder [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2). NPS ruft diese Funktion für jedes gültige Authentifizierungs-oder Buchhaltungs Paket auf, das von dem Netzwerk Zugriffs Server (NAS) empfangen wird. NPS ruft diese Funktionen in jeder der DLLs auf, die unter dem [Registrierungsschlüssel](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)für die NPS-Parameter aufgeführt sind. Die DLLs werden in der Reihenfolge aufgerufen, in der Sie aufgelistet sind.

Wenn eine NPS-Erweiterungs-DLL mehr als eine der oben genannten Funktionen exportiert, ruft NPS nur eine dieser Funktionen auf: die neueste Funktion, die vom Betriebssystem unterstützt wird.

> [!Note]  
> IAS hat ursprünglich nur [*radiusextensionprocess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process)unterstützt. IAS unterstützt auch [*radiusextensionprocessex*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex). IAS (und spätere NPS) unterstützt auch [*RadiusExtensionProcess2*](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2).

 

NPS-Erweiterungs-DLLs können auch [**radiusextensioninit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) -und [**radiusextensionterm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) -Funktionen exportieren. Wenn Sie vorhanden sind, ruft NPS diese Funktionen auf, wenn der Dienst gestartet bzw. beendet wird.

## <a name="radiusextensionprocess-callback-function"></a>Radiusextensionprocess-Rückruffunktion

In einer DLL der Authentifizierungs Erweiterung empfängt [*radiusextensionprocess*](/windows/desktop/api/authif/nc-authif-pradius_extension_process) alle Attribute, die von NPS in der Authentifizierungs-oder Buchhaltungs Anforderung empfangen werden. Mithilfe dieser Attribute kann die Funktion zusätzliche Überprüfungen durchführen, die Autorisierungen des Benutzers überprüfen oder Buchhaltungsdaten Sätze an einen zentralen Zustands Server senden.

In einer Autorisierungs Erweiterungs-DLL empfängt **radiusextensionprocess** alle Attribute, die vom NPS-Autorisierungs Dienst generiert werden. Dabei handelt es sich um die Attribute, die im Access-Accept Paket zurückgegeben werden.

Nach dem Aufrufen von **radiusextensionprocess** hängt die von NPS ausgeführte Aktion vom Rückgabewert von **radiusextensionprocess** und dem Wert ab, der im *pfaction* -Parameter zurückgegeben wird. Diese Werte sind in der folgenden Tabelle aufgeführt.



| *pfaction* | Authentifizierungs-Erweiterungs-DLL                                                                                                                                            | Autorisierungs Erweiterungs-DLL                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Akzeptieren     | Umgeht alle weiteren authentifizierungserweiterungs-DLLs und umgeht auch den NPS-Authentifizierungsmechanismus.                                                                  | Accept ist unzulässig.                                                                                                                                         |
| Reject     | Umgeht alle weiteren authentifizierungserweiterungs-DLLs und umgeht auch den NPS-Authentifizierungsmechanismus. Access-Reject Paket wird gesendet.                                    | Umgeht alle weiteren Autorisierungs Erweiterungs-DLLs.                                                                                                          |
| Weiter   | Das Paket wird an die nächste authentifizierungserweiterungs-dll oder an den NPS-Authentifizierungsmechanismus gesendet, wenn in der Registrierung keine weiteren DLLs der Authentifizierungs Erweiterung aufgeführt sind. | Das Paket wird an die nächste Autorisierungs Erweiterungs-DLL oder an das NPS-Buchhaltungs Protokoll gesendet, wenn keine weiteren Autorisierungs Erweiterungs-DLLs in der Registrierung aufgeführt sind. |



 

**Wenn für** alle Erweiterungs-DLLs ein Fehler zurückgegeben wird, wird das Paket verworfen. Pakete, die aufgrund eines Fehlers verworfen werden, werden nicht vom NPS-Buchhaltungs Protokoll verarbeitet.

Wenn ein Fehler auftritt, stellt NPS ein generisches Fehler Ereignis an das Ereignisprotokoll an. Es wird empfohlen, dass die Erweiterungs-DLL zusätzliche Fehler Protokollierung bereitstellt.

Weitere Informationen und ein Diagramm, das den vorangehenden Prozess darstellt, finden Sie unter [Informationen zu NPS-Erweiterungen](/windows/desktop/Nps/ias-about-internet-authentication-service).

**Radiusextensionprocess** sollte einen Fehler zurückgeben, wenn die Annahme oder Ablehnung des Pakets nicht überprüft werden kann. Diese Situation kann auftreten, wenn durch ein Netzwerkproblem verhindert wird, dass **radiusextensionprocess** mit der Benutzer Authentifizierungs Datenbank kommuniziert.

Bei der Verarbeitung eines Buchhaltungs Pakets ist der *pfaction* -Parameter **null**, daher kann *pfaction* nicht festgelegt werden. Wenn bei der Verarbeitung einer Buchhaltungs Anforderung ein Fehler von der **radiusextensionprocess** -Funktion zurückgegeben wird, wird die Anforderung von NPS verworfen.

> [!Note]  
> Nachdem ein Accept-Vorgang empfangen wurde, ruft NPS in den verbleibenden DLLs in der Sequenz nicht **radiusextensionprocess** auf. Da einige Authentifizierungsfunktionen auch Autorisierungen implementieren können, kann das Überspringen solcher Authentifizierungsfunktionen dazu führen, dass Autorisierungen ausgelassen werden. Wenn eine Instanz von [**radiusextensionprocess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) Accept zurückgibt, ist es wichtig, keine Annahmen über die abgerufenen Autorisierungen zu treffen.

 

Wenn Continue oder Accept zurückgegeben wird, wird das Profil, das dem Bereich entspricht, im Access-Accept Paket zurückgesendet.

Authentifizierungserweiterungs-DLLs sollten für die Koexistenz mit den integrierten NPS-Authentifizierungs Anbietern und anderen Erweiterungs-DLLs entworfen werden. Wenn eine Erweiterung nur auf eine bestimmte Benutzerdatenbank (z. b. Windows Active Directory) anwendbar ist, sollte Sie vor der Verarbeitung der Anforderung das in den *pattrs* -Parametern übergebenen [**ratprovider**](/windows/desktop/api/authif/ne-authif-radius_authentication_provider) -Attribut überprüfen. Das ratprovider-Attribut wäre eine einer Liste von Attributen, auf die der *pattrs* -Parameter verweist.

Erweiterungs-DLLs sollten keine Anforderungen ablehnen, da erforderliche Attribute fehlen. Wenn eine Authentifizierungs Erweiterung z. b. das User-Password-Attribut, ratuserpassword, erfordert und das-Attribut nicht vorhanden ist, sollte die Erweiterung eine Aktion von racontinue zurückgeben, um anderen Erweiterungen und Anbietern die Möglichkeit zu geben, die Anforderung zu verarbeiten.

NPS Ruft die [**radiusextensionprocess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) -Funktion auf, nachdem die Entscheidung getroffen wurde, eine bestimmte Authentifizierungs Datenbank zu verwenden, aber bevor der Benutzer authentifiziert wird. Daher sind Informationen darüber, welche Authentifizierungs Datenbank verwendet werden soll, für die Funktion verfügbar, damit die Funktion die Autorisierungen des Benutzers in der entsprechenden Authentifizierungs Datenbank überprüfen kann. NPS unterstützt verschiedene Authentifizierungs Datenbanken, einschließlich des Windows-Active Directory.

## <a name="radiusextensionprocessex-callback-function"></a>Radiusextensionprocessex-Rückruffunktion

NPS-Erweiterungs-DLLs können [**radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) anstelle von oder zusätzlich zu [**radiusextensionprocess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)exportieren. Diese Funktion ermöglicht der dll, zusätzliche Autorisierungs Attribute an die Authentifizierungs Antwort anzufügen.

Die im Abschnitt " *radiusextensionprocess" der Rückruffunktion* beschriebenen Informationen gelten für die [**radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) -Funktion.

[**Radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) kann keines der Attribute ändern oder entfernen, die vorhanden sind. Wenn ein Szenario auftritt, in dem die dll Attribute ändern oder entfernen muss, besteht die einzige Möglichkeit darin, die NPS-Benutzeroberfläche zu verwenden, um sicherzustellen, dass die Attribute nicht vorhanden sind. Standardmäßig sind keine Autorisierungs Attribute vorhanden. Alle vorhandenen müssen über die Benutzeroberfläche hinzugefügt worden sein.

Wenn mehrere Autorisierungs-DLLs konfiguriert sind und einige dieser DLLs [**radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)implementieren, empfängt die **radiusextensionprocess/Ex-** Funktion in einer bestimmten dll nicht die Attribute von den zuvor aufgerufenen DLLs der Autorisierung. Er empfängt nur die Attribute, die vom NPS-Autorisierungs Dienst generiert werden.

## <a name="radiusextensionprocess2-callback-function"></a>RadiusExtensionProcess2-Rückruffunktion

NPS-Erweiterungs-DLLs können auch [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) anstelle von oder zusätzlich zu [**radiusextensionprocess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) und **radiusextensionprocessex** exportieren. Diese Funktion ermöglicht der dll, Attribute zur Authentifizierungsanforderung oder-Antwort hinzuzufügen, zu ändern und zu entfernen.

Die gleichen Informationen, die im Abschnitt *radiusextensionprocessex Callback-Funktion* beschrieben werden, gelten für die [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex) -Funktion mit den folgenden Ausnahmen:

-   In einer Autorisierungs-dll empfängt **RadiusExtensionProcess2** sowohl die vom NPS-Autorisierungs Dienst generierten Attribute als auch die Attribute, die zuvor als Autorisierungs-DLLs generiert wurden.
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) verfügt über keinen *pfaction* -Parameter. **RadiusExtensionProcess2** legt die endgültige Disposition der Anforderung mithilfe der [**setresponsetype**](/previous-versions/ms688462(v=vs.85)) -Funktion fest, die in der [**RADIUS- \_ Erweiterungs \_ Steuerungs \_ Block**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) -Struktur bereitgestellt wird.
-   NPS ruft immer die [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) -Funktion in allen verbleibenden DLLs auf, unabhängig davon, ob Funktionen in früheren DLLs akzeptiert haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der Erweiterungs-DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Benutzer Identifizierungs Attribute](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 