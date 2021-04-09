---
description: Die Zertifikat Dienste bieten Webregistrierungs Seiten, die zum Anfordern von Zertifikaten verwendet werden können.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Anpassen der Webregistrierungs Seiten der Zertifikat Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb2fbf421eceb1ebf0b15379aca5d0788a992ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868428"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Anpassen der Webregistrierungs Seiten der Zertifikat Dienste

Die [*Zertifikat Dienste*](../secgloss/c-gly.md) bieten Webregistrierungs Seiten, die zum Anfordern von Zertifikaten verwendet werden können. Ein Administrator kann einige der Elemente anpassen, die auf den Webregistrierungs Seiten angezeigt werden können. Sie sollten sich jedoch mit den Webregistrierungs Seiten und der Webskript Erstellung vertraut machen, bevor Sie Änderungen vornehmen. Weitere Informationen zu Webskripts finden Sie unter [Skripting](/previous-versions/ms950396(v=msdn.10)).

Die Standardwerte für die Felder Distinguished Name für Organisation, Organisationseinheit, Ort, Bundesland und Land/Region sind die für die Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) angegebenen Werte, wenn die Zertifikat Dienste installiert sind. Diese Standardwerte werden auf den Webseiten angezeigt und können vom Benutzer während der Zertifikat Registrierung geändert werden. Wenn jedoch andere Standardwerte in den Webseiten angezeigt werden sollen, können Sie die Datei "certdat. Inc" (im Pfad \\ *WindowsDirectory* \\ system32 \\ certrv) bearbeiten \\ . insbesondere können Sie den folgenden Variablen, die für die Anpassung bereitgestellt werden, benutzerdefinierte Werte zuweisen.



| Variable            | BESCHREIBUNG                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sdefaultcompany     | Standard Unternehmen (wird in der [*Zertifikat Anforderung*](../secgloss/c-gly.md) als [*X. 509*](../secgloss/x-gly.md) -Organisations Feld angezeigt). |
| sdefaultor gunit     | Standard Abteilung (wird in der Zertifikat Anforderung als X. 509-Organisations Einheits Feld angezeigt).                                                                                                                                           |
| sdefaultlokalität    | Standard Stadt (wird in der Zertifikat Anforderung als X. 509-Speicherort Feld angezeigt).                                                                                                                                                            |
| sdefaultstate       | Standard State/Province (wird in der Zertifikat Anforderung als X. 509-Status Feld angezeigt).                                                                                                                                                     |
| sdefaultcountry     | Standardland/-Region (wird in der Zertifikat Anforderung als X. 509-Feld "Land/Region" angezeigt).                                                                                                                                            |
| npdingtimeoutdays | Anzahl der Tage, in denen der Benutzer ein ausstehendes Zertifikat abrufen kann, nachdem es angefordert wurde.                                                                                                                                          |



 

In der Datei "certdat. Inc" sollten keine anderen Variablen geändert werden.

Im folgenden Beispiel wird die Standard Organisationseinheit auf "Marketing" festgelegt.


```VB
sDefaultOrgUnit="Marketing"
```



Außerdem können Sie die Datei "certrqtp. Inc" Bearbeiten, um dem Benutzer verfügbare [*Zertifikat Vorlagen*](../secgloss/c-gly.md) oder-Typen hinzuzufügen, zu ändern oder zu entfernen. Diese Vorlagen und Typen sowie zugehörige Informationen sind in einem dimensionierten Array namens rgAvailReqTypes (*m*, 5) enthalten.

Dieses Array ist wie alle Visual Basic Scripting Edition Arrays NULL basiert, und die erste Dimension ( *m*) des Arrays weist den Arbeitsspeicher für *m*+ 1-Elemente zu. Wenn Sie beim Anpassen der Webseiten die Anzahl der Elemente im rgAvailReqTypes-Array ändern müssen, legen Sie für die *m* -Dimension einen Wert fest, der kleiner als die Gesamtzahl der benötigten Elemente ist. Wenn Sie z. b. über sieben Zertifikat Vorlagen verfügen, ändern Sie die Deklaration von rgAvailReqTypes, wie im folgenden Beispiel gezeigt.


```VB
Dim rgAvailReqTypes(6,5)
```



Die zweite Dimension des Arrays, die immer den Wert "Five" hat, ordnet die sechs Felder zu, die die einzelnen Elemente bilden. Diese sechs Felder repräsentieren die Zertifikat Vorlage oder den Typ, den dieser Vorlage oder Typ zugeordneten anzeigen Amen und ob die Vorlage " [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME)" erfordert.

Damit Sie leichter erkennen können, auf welche dieser Felder zugegriffen wird, bietet certrqtp. Inc auch die folgenden Konstanten, die Sie beim Festlegen von Feldwerten verwenden können.



| Konstante                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Feld \_ OID**                        | (Gilt für eigenständige Zertifizierungsstellen) Index zum ersten Feld des Elements. stellt einen [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID) für einen Zertifikattyp dar.<br/>                                                                                                           |
| **Feld \_ Vorlage**                   | (Gilt für Unternehmens Zertifizierungsstellen) Index zum ersten Feld des Elements. stellt eine Zertifikat Vorlage dar.<br/>                                                                                                                                                                                                                           |
| **Feld " \_ FriendlyName"**               | Index für das zweite Feld des Elements. stellt den anzeigen Amen (den der Benutzer bei der Anmeldung sehen wird) des Elements im ersten Feld dar.                                                                                                                                                                                               |
| **Feld " \_ csplist"**                    | Index für das dritte Feld des Elements. Eine Liste der [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) -Namen, die von der Vorlage zugelassen werden. Jeder Name in der Liste wird durch ein Fragezeichen (?) getrennt.                                                    |
| **Feld \_ CSPLIST2**                   | Index für das vierte Feld des Elements. Eine sekundäre Liste von [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) -Namen, die von der Vorlage zugelassen werden. Jeder Name in der Liste wird durch ein Fragezeichen (?) getrennt. Diese Liste stellt einen anderen Standardwert bereit. |
| **\_exportier bares Feld**                 | Index zum fünften Feld des Elements. Gibt an, ob die Vorlage angibt, dass der Schlüssel exportierbar sein soll. Wenn dieses Feld "true" enthält, ist der Schlüssel exportierbar. Wenn dieses Feld den Wert "false" enthält, kann der Schlüssel nicht exportiert werden.                                                                                                        |
| **das Feld \_ erfordert \_ SMIME- \_ Funktionen.** | Diese Konstante wird nicht unterstützt.                                                                                                                                                                                                                                                                                                      |



 

Die folgenden Ausdrücke weisen z. b. die OID von 1.3.6.1.5.5.7.3.2 dem ersten Feld des ersten Elements zu und weisen das "Webbrowser Zertifikat" dem zweiten Feld des ersten Elements zu (der Arraywert von 0 (null) indiziert das erste Element).


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



Das Ergebnis dieser Zuweisungen ist, dass der Benutzer bei der Anmeldung das **Textweb Browser-Zertifikat** sieht. wenn der Benutzer das **Webbrowser Zertifikat** auswählt, enthält die [*Zertifikat Anforderung*](../secgloss/c-gly.md) die OID 1.3.6.1.5.5.7.3.2.

Die Datei "certrqtp. Inc" enthält auch Konstanten, die für die anzeigen amen der Zertifikat Vorlagen oder-Typen verwendet werden. Das folgende Beispiel zeigt das Format.


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Diese Konstanten werden in einem Block in der Datei "certrqtp. Inc" definiert, und diese Gruppierung vereinfacht das Zuweisen der einzelnen Benutzer zu einem benutzerdefinierten Wert. Dies ist besonders hilfreich, wenn Sie die anzeigen Amen für internationale Versionen der Webseiten lokalisieren.

Schließlich enthält die Datei "certrqtp. Inc" eine Variable, die die Anzahl der Zertifikat Vorlagen oder-Typen im rgAvailReqTypes-Array darstellt. Im Gegensatz zur *m* -Dimension des Arrays legen Sie den Wert der navailreqtypes-Variablen auf die tatsächliche Anzahl der Zertifikat Vorlagen oder-Typen fest, die von der Installation verwendet werden. Dieser Wert darf nicht größer als *m*+ 1 sein. Obwohl es am Anfang der Datei "certrqtp. Inc" deklariert wurde, wird navailreqtypes ein Wert zugewiesen, nachdem das rgAvailReqTypes-Array aufgefüllt wurde. Dadurch können Sie leichter erkennen, wie viele Elemente tatsächlich vom Array verwendet werden. Der Wert navailreqtypes wird in einer Iterationen an anderer Stelle in den Webregistrierungs Seiten verwendet. Daher ist es wichtig, dass diese Variable genau die Anzahl der Zertifikat Vorlagen oder-Typen widerspiegelt, die für den Benutzer sichtbar sein sollen.

Beachten Sie, dass das Hinzufügen von [*Zertifikat Vorlagen*](../secgloss/c-gly.md) und-Typen zur Datei "certrqtp. Inc" nicht gewährleistet, dass der Benutzer ein Zertifikat mit diesen Merkmalen erhalten kann. die Zertifizierungsstelle muss autorisiert sein, ein Zertifikat für die angegebene Zertifikat Vorlage oder den angegebenen Typ auszustellen.

Installationen können Ihre eigenen Anwendungen oder Webseiten erstellen, um ein Zertifikat anzufordern und zu erhalten. Mit den [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) -und [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) -Objekten können Programmierer oder skriderer Anwendungen für [*Zertifikat Anforderungen*](../secgloss/c-gly.md) erstellen.

Um ein Zertifikat anzufordern, das auf einer [*Smartcard*](../secgloss/s-gly.md)ausgestellt werden soll, können Sie die Smartcard-Registrierungs Steuerung verwenden. Weitere Informationen und Beispielcode finden Sie unter [**iscrdenr**](iscrdenr.md).

 

 
