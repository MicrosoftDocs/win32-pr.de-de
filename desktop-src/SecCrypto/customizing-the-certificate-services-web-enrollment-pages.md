---
description: Zertifikatdienste stellen Webregistrierungsseiten bereit, die zum Anfordern von Zertifikaten verwendet werden können.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Anpassen der Webregistrierungsseiten für Zertifikatdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0132ce4e5e1fef588ffc429597717433dd1b780d2f7f35f9c886f1978b5b318a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767795"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Anpassen der Webregistrierungsseiten für Zertifikatdienste

[*Zertifikatdienste*](../secgloss/c-gly.md) stellen Webregistrierungsseiten bereit, die zum Anfordern von Zertifikaten verwendet werden können. Ein Administrator kann einige der Elemente anpassen, die auf den Webregistrierungsseiten angezeigt werden können. Sie sollten jedoch mit den Webregistrierungsseiten und der Webskripterstellung vertraut sein, bevor Sie Änderungen vornehmen. Weitere Informationen zur Webskripterstellung finden Sie unter [Skripterstellung.](/previous-versions/ms950396(v=msdn.10))

Die Standardwerte für die Felder Distinguished Name (Distinguished Name) für Organisation, Organisationseinheit, Ort, Bundesstaat und Land/Region sind die Werte, die bei der Installation der Zertifikatdienste für die [*Zertifizierungsstelle*](../secgloss/c-gly.md) angegeben werden. Diese Standardwerte werden auf den Webseiten angezeigt und können vom Benutzer während des Zertifikatregistrierungsprozesses geändert werden. Wenn jedoch andere Standardwerte auf den Webseiten angezeigt werden sollen, können Sie die Datei Certdat.inc bearbeiten (im Pfad \\ *WindowsDirectory* \\ System32 \\ Certsrv). \\ Insbesondere können Sie den folgenden Variablen benutzerdefinierte Werte zur Anpassung zuweisen.



| Variable            | Beschreibung                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | Standardunternehmen (wird in der [*Zertifikatanforderung*](../secgloss/c-gly.md) als [*Feld X.509-Organisation*](../secgloss/x-gly.md) angezeigt). |
| sDefaultOrgUnit     | Standardabteilung (wird in der Zertifikatanforderung als Feld X.509-Organisationseinheit angezeigt).                                                                                                                                           |
| sDefaultLocality    | Standardort (wird in der Zertifikatanforderung als Feld X.509-Standort angezeigt).                                                                                                                                                            |
| sDefaultState       | Standardzustand/Kanton (wird in der Zertifikatanforderung als Feld X.509 State angezeigt).                                                                                                                                                     |
| sDefaultCountry     | Standardland/-region (wird in der Zertifikatanforderung als Feld X.509 Country/Region angezeigt).                                                                                                                                            |
| nPendingTimeoutDays | Anzahl der Tage, in denen der Benutzer ein ausstehendes Zertifikat abrufen kann, nachdem es angefordert wurde.                                                                                                                                          |



 

In der Datei "Certdat.inc" sollten keine anderen Variablen geändert werden.

Im folgenden Beispiel wird die Standardorganisationseinheit auf "Marketing" festgelegt.


```VB
sDefaultOrgUnit="Marketing"
```



Darüber hinaus können Sie die Datei Certrqtp.inc bearbeiten, um [*Zertifikatvorlagen*](../secgloss/c-gly.md) oder -typen hinzuzufügen, zu ändern oder zu entfernen, die dem Benutzer zur Verfügung stehen. Diese Vorlagen und Typen sowie verwandte Informationen sind in einem dimensionierten Array namens rgAvailReqTypes(*m*, 5) enthalten.

Dieses Array ist wie alle Visual Basic Scripting Edition-Arrays nullbasiert, und daher belegt die erste Dimension des Arrays, *m,* Arbeitsspeicher für *m*+1 Elemente. Wenn Sie die Webseiten anpassen, müssen Sie daher die Anzahl der Elemente im rgAvailReqTypes-Array ändern, indem Sie die *m-Dimension* auf einen wert kleiner als die Gesamtzahl der benötigten Elemente festlegen. Wenn Sie beispielsweise über sieben Zertifikatvorlagen verfügen, ändern Sie die Deklaration von rgAvailReqTypes wie im folgenden Beispiel gezeigt.


```VB
Dim rgAvailReqTypes(6,5)
```



Die zweite Dimension des Arrays, die immer den Wert 5 aufweist, ordnet die sechs Felder zu, aus denen jedes Element besteht. Diese sechs Felder stellen die Zertifikatvorlage oder den Zertifikattyp, den Anzeigenamen, der dieser Vorlage oder diesem Typ zugeordnet ist, und ob die Vorlage [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) erfordert.

Damit Sie leichter nachvollziehen können, auf welche dieser Felder zugegriffen wird, stellt Certrqtp.inc auch die folgenden Konstanten bereit, die Sie beim Festlegen von Feldwerten verwenden können.



| Konstante                              | Beschreibung                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FIELD \_ OID**                        | (Gilt für eigenständige ZS) Index für das erste Feld des Elements; stellt einen [*Objektbezeichner*](../secgloss/o-gly.md) (OID) für einen Zertifikattyp dar.<br/>                                                                                                           |
| **\_FELDVORLAGE**                   | (Gilt für Unternehmens-CAs) Index für das erste Feld des Elements; stellt eine Zertifikatvorlage dar.<br/>                                                                                                                                                                                                                           |
| **FIELD \_ FRIENDLYNAME**               | Index für das zweite Feld des Elements; stellt den Anzeigenamen (der dem Benutzer bei der Registrierung angezeigt wird) des Elements im ersten Feld dar.                                                                                                                                                                                               |
| **FIELD \_ CSPLIST**                    | Index zum dritten Feld des Elements. Eine Liste der von der Vorlage zulässigen Namen von [*Kryptografiedienstanbietern.*](../secgloss/c-gly.md) Jeder Name in der Liste ist durch ein Fragezeichen (?) getrennt.                                                    |
| **FIELD \_ CSPLIST2**                   | Index zum vierten Feld des Elements. Eine sekundäre Liste der namen [*kryptografischer Dienstanbieter,*](../secgloss/c-gly.md) die von der Vorlage zugelassen werden. Jeder Name in der Liste ist durch ein Fragezeichen (?) getrennt. Diese Liste enthält einen anderen Standardwert. |
| **FELD \_ EXPORTIERBAR**                 | Index für das fünfte Feld des Elements. Gibt an, ob die Vorlage angibt, dass der Schlüssel exportierbar sein soll. Wenn dieses Feld "True" enthält, kann der Schlüssel exportiert werden. Wenn dieses Feld "False" enthält, kann der Schlüssel nicht exportiert werden.                                                                                                        |
| **FELD \_ BENÖTIGT \_ SMIME-FUNKTIONEN \_** | Diese Konstante wird nicht unterstützt.                                                                                                                                                                                                                                                                                                      |



 

Die folgenden Ausdrücke weisen z. B. die OID von 1.3.6.1.5.5.7.3.2 dem ersten Feld des ersten Elements zu und weisen dem zweiten Feld des ersten Elements "Webbrowserzertifikat" zu (der Arraywert null indiziert das erste Element).


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



Das Ergebnis dieser Zuweisungen ist, dass dem Benutzer bei der Registrierung der Text **Webbrowserzertifikat** angezeigt wird, und wenn der Benutzer **Webbrowserzertifikat** auswählt, enthält die [*Zertifikatanforderung*](../secgloss/c-gly.md) die OID 1.3.6.1.5.5.7.3.2.

Die Datei Certrqtp.inc enthält auch Konstanten, die für die Anzeigenamen der Zertifikatvorlagen oder -typen verwendet werden. Das folgende Beispiel zeigt das Format.


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Diese Konstanten werden in einem -Block in der Datei Certrqtp.inc definiert, und diese Gruppierung erleichtert es, jedem von ihnen einen benutzerdefinierten Wert zuzuweisen. Dies ist besonders hilfreich, wenn Sie die Anzeigenamen für internationale Versionen der Webseiten lokalisieren.

Schließlich enthält die Datei Certrqtp.inc eine Variable, die die Anzahl der Zertifikatvorlagen oder -typen im Array rgAvailReqTypes darstellt. Legen Sie im Gegensatz zur *m-Dimension* des Arrays den Wert der nAvailReqTypes-Variablen auf die tatsächliche Anzahl von Zertifikatvorlagen oder -typen fest, die von der Installation verwendet werden. dieser Wert darf nicht größer als *m*+1 sein. Obwohl nAvailReqTypes am Anfang der Datei Certrqtp.inc deklariert wurde, wird nAvailReqTypes nach dem Auffüllen des rgAvailReqTypes-Arrays ein Wert zugewiesen, sodass einfacher zu erkennen ist, wie viele Elemente tatsächlich vom Array verwendet werden. Der nAvailReqTypes-Wert wird in einer Iteration an anderer Stelle auf den Webregistrierungsseiten verwendet. Daher ist es wichtig, dass diese Variable die Anzahl der Zertifikatvorlagen oder -typen genau widerspiegelt, die für den Benutzer angezeigt werden sollen.

Beachten Sie, dass das einfache Hinzufügen von [*Zertifikatvorlagen*](../secgloss/c-gly.md) und -typen zur Datei "Certrqtp.inc" nicht garantiert, dass der Benutzer ein Zertifikat mit diesen Merkmalen erhalten kann. Die Zertifizierungsstelle muss autorisiert sein, ein Zertifikat für die angegebene Zertifikatvorlage oder den angegebenen Zertifikattyp auszustellen.

Installationen können eigene Anwendungen oder Webseiten erstellen, um ein Zertifikat anzufordern und zu empfangen. Die [**Objekte ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) und [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) ermöglichen Programmierern oder Skriptern das Erstellen von [*Zertifikatanforderungsanwendungen.*](../secgloss/c-gly.md)

Um anzufordern, dass ein Zertifikat auf einer [*Smartcard*](../secgloss/s-gly.md)ausgestellt wird, können Sie die Smartcard-Registrierungssteuerung verwenden. Weitere Informationen und Beispielcode finden Sie unter [**ISCrdEnr**](iscrdenr.md).

 

 
