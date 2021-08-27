---
title: Online-Musik Store ins Board
description: Online-Musik Store ins Board
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Windows Media Player Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcff5aeed04ff2e60b03e7b546de23f1d0d747b9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477206"
---
# <a name="getting-an-online-music-store-on-board"></a>Online-Musik Store ins Board

In diesem Thema wird beschrieben, wie Sie einen digitalen Onlinemedienspeicher für Windows Media Player ins Boot holen. Die erforderliche Zeit für das Onboarding von Anfang bis Ende beträgt ca. 45-60 WERKTAGE. Die beiden Phasen des Onboardingprozesses werden in der folgenden Tabelle beschrieben.




| Phase | BESCHREIBUNG | 
|-------|-------------|
| Ausstehend | <ul><li>Sie senden Microsoft die erforderlichen Kontaktinformationen, Startinformationen und Überprüfungskonten.</li><li>Microsoft sendet Ihnen einen Testschlüssel und einen Produktionsschlüssel.</li><li>Sie testen Ihren Onlineshop mit Windows Media Player.</li><li>Sie übermitteln signierte Verträge und Verträge an Microsoft.</li></ul> | 
| Überprüfen | Microsoft überprüft Ihren Onlineshop. | 




 

Nachdem Sie die Ausstehende Phase und die Überprüfungsphase abgeschlossen haben, veröffentlicht Microsoft Ihren Onlineshop.

## <a name="pending-stage"></a>Ausstehende Phase

Die Phase "Ausstehend" bietet Ihnen die Möglichkeit, Ihren Onlineshop in Windows Media Player zu testen. Es ist auch ein guter Zeitpunkt, sicherzustellen, dass alle erforderlichen Vereinbarungen und Verträge unterzeichnet werden. Senden Sie Microsoft zunächst die folgenden Informationen, wie weiter unten in diesem Thema definiert:

-   Kontaktinformationen
-   Startinformationen
-   Überprüfungskonten

Nach Erhalt Ihrer Kontakt- und Startinformationen sendet Microsoft Ihnen einen Testschlüssel und einen Produktionsschlüssel. Nachdem Sie Ihren Testschlüssel zur Registrierung hinzugefügt und den Player neu gestartet haben, wird Ihr Onlineshop im Player angezeigt, und Sie können ihn testen. Informationen dazu, wo Der Testschlüssel in der Registrierung gespeichert werden soll, finden Sie unter [Registrierungsschlüssel und -einträge für eine Online-Store vom Typ 1](registry-keys-and-entries-for-a-type-1-online-store.md) oder [Registrierungsschlüssel und -einträge für einen Typ 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).

Sie sollten alle Aspekte Ihres Onlineshops testen, einschließlich der Benutzeroberfläche und des Plug-Ins. Im Rahmen des Testprozesses müssen Sie die tests ausführen, die unter [Validierungstests für Typ 2 Online Musik Stores](validation-tests-for-type-2-online-music-stores.md)beschrieben sind.

> [!Note]  
> Speicher vom Typ 1 müssen alle Validierungstests für Speicher vom Typ 2 sowie einige zusätzliche Tests bestehen, die für die Art 1 spezifisch sind. Informationen zu Typ 1-Validierungstests erhalten Sie vom Windows Media Player Services Virtual Team unter mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Kontaktinformationen

In der folgenden Tabelle sind die Kontaktinformationen aufgeführt, die Microsoft für Ihren Onlineshop benötigt. Füllen Sie das [Formular Kontaktinformationen](contact-information-form-for-an-online-music-store.md) aus, und senden Sie es an das Windows Media Player Services Virtual Team unter mpsvctm@microsoft.com .



| Element                     | BESCHREIBUNG                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Store Name               | Der Markenname Ihres Geschäfts                                                            |
| Anbietername            | Der Name des Anbieters bzw. des White label-Unternehmens (falls anders)                               |
| Store Locale             | Die Windows Gebietsschemas ihres Geschäfts müssen in angezeigt werden.                                |
| Store Kategorie           | Musik, Radio, Film, TV, Sport, News, Audiounterhaltung und/oder Sonstiges (beschreiben Sie es bitte) |
| Kaufmodell           | Kauf, Verleih, Abonnement und/oder Sonstiges (beschreiben Sie es bitte)                            |
| Store Sprache           |                                                                                           |
| Store Kontaktname(en)    |                                                                                           |
| Store Kontakt-E-Mail(s)  |                                                                                           |
| MSFT Passport-Konten | Dies ist für mögliche zukünftige Nominierungen in Beta- und Partnerentwicklungsprogrammen vorgesehen.         |
| Lieferadresse         | Keine P.O. Boxen                                                                             |
| City                     |                                                                                           |
| State                    |                                                                                           |
| Postleitzahl              |                                                                                           |
| Land/Region           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Umfragekontakt           | Ist es in Ordnung, wenn wir uns in Zukunft mit Ihnen in Verbindung setzen?        |



 

## <a name="startup-information"></a>Startinformationen

Senden Sie Microsoft für jede geografische Region, die Ihr Store bedienen wird, eine Reihe von Startinformationen für Ihren Testspeicher, eine Reihe von Startinformationen für Ihren Produktionsspeicher und eine Reihe von Überprüfungskonten.

Das Thema [Startinformationsformular für eine Online-Musik Store](startup-information-form-for-an-online-music-store.md) enthält zwei Kopien des Formulars Startinformationen und eine Kopie des Formulars "Überprüfungskonten". Füllen Sie die Formulare aus, und senden Sie sie an das Windows Media Player Services Virtual Team unter mpsvctm@microsoft.com .

In der folgenden Tabelle werden die Startinformationen beschrieben, die Microsoft für Ihren Onlineshop benötigt.



| Element                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XML-URL für Dienstinformationen (Grenzwert von 2048 Zeichen)                                                              | Die URL, unter der Windows Media Player Ihr [ServiceInfo-XML-Dokument](serviceinfo-document.md)abruft.                                                                                                                                         |
| Dienstschlüssel (eindeutige ID)                                                                                  | Eine Zeichenfolge, die Ihren Onlineshop eindeutig identifiziert. Sie sollten einen für die Produktion und einen für Tests erstellen (z. B. "MyStore" und "MyStoreTest"). Beachten Sie, dass ein Dienstschlüssel nicht mit einem Testschlüssel identisch ist.                        |
| Anzeigename (Grenzwert von 30 Zeichen)                                                                       | Der Name Ihres Geschäfts, der in der Windows Media Player Dienstauswahl angezeigt wird.                                                                                                                                                        |
| Menübild-URL (Grenzwert von 2048 Zeichen)                                                                    | Die URL, unter der Windows Media Player das logo mit 15 x 15 Pixeln abruft, das in der Dienstauswahl angezeigt wird.                                                                                                                                 |
| Kaufen Musik URL (Limit für 2048 Zeichen)<br/> (Nur integrierte Musikspeicher)<br/>                | Die URL, die von den Playerlinks "CD kaufen" und "Shop for Musik Online" verwendet wird.                                                                                                                                                              |
| Kauf-URL mit einer Benutzeroberfläche von 10 Fuß (Grenzwert von 2048 Zeichen)<br/> (Nur integrierte Musikspeicher – optional)<br/> | Die URL, die von den Playerlinks "CD kaufen" und "Shop for Musik Online" in Windows XP Media Center Edition und in Windows Media Center in Windows Vista verwendet wird.                                                                              |
| Store Logo (130w x 30h)<br/> (Fügen Sie die PNG-Datei separat an.)<br/>                              | Das Storelogo, das in der QuickInfo angezeigt wird, die angezeigt wird, wenn sich der Mauszeiger über dem Bild für alle Durchsuchen befindet. Dieses Logo muss eine PNG-formatierte Datei sein und vorzugsweise alphageblendet sein, damit es an Farbänderungen in Windows Media Player angepasst werden kann. |
| Browse-all Image (108w x 108h)<br/> (Fügen Sie die PNG-Datei separat an.)<br/>                       | Die kurze Beschreibung in der QuickInfo, die angezeigt wird, wenn sich der Mauszeiger über dem Bild mit dem gesamten Durchsuchen befindet.                                                                                                                                               |
| Store Beschreibungstext (Grenzwert von 110 Zeichen)                                                             | Der Text, der in der QuickInfo unterhalb des Speicherbeschreibungstexts angezeigt wird.                                                                                                                                                                        |
| Text für Link (Grenzwert von 45 Zeichen)                                                                  | Das Storelogo, das auf der Seite Alle Onlineshops durchsuchen angezeigt wird. Es muss sich um eine PNG-formatierte Datei und vorzugsweise um eine Alphablended-Datei mit Farbänderungen in Windows Media Player.                                           |



 

> [!Note]  
> Das 108 x 108 Pixel große Bild "Browse-All" ist eine Voraussetzung für Windows Media Player 11 und höher.

 

> [!Note]  
> In Windows Media Player 11 und höher werden die Elemente ServiceTask2 und ServiceTask3 des ServiceInfo-XML-Dokuments ignoriert. Ausführliche Informationen zum ServiceInfo-XML-Dokument finden Sie unter [ServiceInfo-Dokument.](serviceinfo-document.md)

 

## <a name="validation-accounts"></a>Überprüfungskonten

Microsoft benötigt fünf (5) Validierungskonten für jeden Kontotyp, den Ihr Onlineshop anbietet, um den im folgenden Abschnitt überprüfungsphase beschriebenen Überprüfungsprozess abschließen zu können. Wenn Sie beispielsweise Konten anbieten, die zwischen Features und Funktionen wie Basic und Premium unterscheiden, benötigt Microsoft fünf (5) Validierungskonten für jeden Typ, für insgesamt zehn (10) Konten.

Senden Sie den Benutzernamen und das Kennwort für jedes Validierungskonto an mpsvctm@microsoft.com . Geben Sie auch den Namen einer Person an, die Microsoft in Bezug auf Validierungskonten kontaktieren kann. Diese Konten werden für die laufende monatliche Überprüfung verwendet. Schließen Sie daher einen Prozess zum "Erneuten Aufladen" der Konten ein. Eines der häufigsten Probleme tritt auf, wenn ein Onlineshop kein ausreichendes Kaufguthaben für Microsoft bereitstellen kann, um alle Kaufszenarien zu überprüfen. Die Konten müssen aktiv bleiben, nachdem das Onboarding abgeschlossen ist.

## <a name="validation-stage"></a>Überprüfungsphase

Während der Überprüfungsphase überprüft Microsoft, ob die hauptfunktionen Ihres Onlineshops ordnungsgemäß funktionieren. Für alle Filialen (Typ 1 und Typ 2) führt Microsoft die Überprüfungstests aus, die unter Validierungstests für Typ 2 Online Musik [Stores ausführlich sind.](validation-tests-for-type-2-online-music-stores.md) Microsoft führt auch einige zusätzliche Validierungstests für Filialen vom Typ 1 aus. Wenn Sie Fragen zur Überprüfungsphase für Speicher vom Typ 1 haben, senden Sie eine E-Mail an mpsvctm@microsoft.com .

Während der Überprüfungsphase durchläuft Microsoft zwei Validierungsläufe. Der erste Durchgang gilt für Release Candidate 1 (RC1) Ihres Onlineshops. Wenn Ihr Speicher die RC1-Überprüfung besteht, sollten Sie ihn sperren und keine weiteren Änderungen vornehmen. Microsoft führt einen zweiten Überprüfungspass in Ihrem Store durch, auch wenn Ihr Store die RC1-Überprüfung besteht.

Wenn ihr Speicher einen Teil des RC1-Validierungspasses nicht erfolgreich ist, haben Sie zwei Wochen Zeit, einen zweiten Release Candidate (RC2) zu erstellen, den Microsoft während des RC2-Validierungstests überprüft.

Wenn in Ihrem Speicher ein Teil der RC2-Überprüfung fehlschlägt, müssen Sie bis zum folgenden Start warten.

## <a name="test-and-production-keys"></a>Test- und Produktionsschlüssel

Denken Sie daran, dass Sie microsoft während der ausstehenden Phase zwei Sätze von Startinformationen gesendet haben: einen für Ihren Testspeicher und einen für Ihren Produktionsspeicher. Denken Sie auch daran, dass Microsoft Ihnen zwei Schlüssel gesendet hat: einen Testschlüssel und einen Produktionsschlüssel.

Der Testschlüssel ist vollständig für Ihre eigene Verwendung. Wenn sich Ihr Testschlüssel in der Registrierung befindet, verwendet Windows Media Player die ServiceInfo-URL, die Sie für Ihren Testspeicher übermittelt haben.

Wenn sich Ihr Produktionsschlüssel in der Registrierung befindet, verwendet Windows Media Player die ServiceInfo-URL, die Sie für Ihren Produktionsspeicher übermittelt haben. Microsoft verwendet Ihren Produktionsschlüssel während der Überprüfungsphase. Microsoft verwendet niemals Ihren Testschlüssel für die Validierung.

Wenn Ihr Store live ist, Windows Media Player die ServiceInfo-URL, die Sie für Ihren Produktionsspeicher übermittelt haben.

Im Allgemeinen sollte Ihr Testspeicher der Ort sein, an dem Sie Ihren Dienst entwickeln und tägliche Änderungen vornehmen. Ihr Produktionsspeicher sollte der Ort sein, an dem Sie eine stabile Version Ihres Diensts behalten.

## <a name="common-on-boarding-problems"></a>Häufige Probleme beim Einsteigen

Im Nachfolgend finden Sie einige häufige Probleme, die dazu führen können, dass der Speicher validierungstests nicht erfolgreich ist.

-   Fehler beim Übergang von Testservern zu Produktionsservern. Dies führt zu vielen Problemen, z. B. fehlende Seiten, ungültigen IIS und Sicherheitseinstellungen und Testkonten, die nicht mehr funktionieren.
-   Der Link Kaufen (oder Shoplink) im Bereich Jetzt wiedererlangt ist ungültig. Dies kann dazu führen, dass die Überprüfung ihres Speichers fehlschlägt, auch wenn alles andere funktioniert.
-   Das Validierungsteam von Microsoft teste verschiedene Kaufszenarien, die von kleinen Käufen bis hin zu sehr großen Käufen reichen. Sie müssen ihnen eine gute Möglichkeit bieten, als Verbraucher in Ihrem Geschäft zu fungieren. Ihr Store kann nicht überprüft werden, wenn das Überprüfungsteam nicht über genügend Kaufguthaben verfügt, um all diese Szenarien zu überprüfen.

Eine vollständige Liste der häufigen Probleme beim Einsteigen und häufig gestellte Fragen, die vom virtuellen Windows Media Player Services-Team kompiliert wurden, finden Sie unter Common [On-Board Problems for Online Musik Stores](common-on-boarding-problems-for-online-music-stores.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Welcome Kit für Onlineshops](online-stores-welcome-kit.md)
</dt> </dl>

 

 





