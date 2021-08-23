---
title: Behandeln von Fehlern bei der Signatur von App-Paketen
description: Ein Fehler bei der App-Bereitstellung kann durch einen Fehler beim Überprüfen der digitalen Signatur des App-Pakets verursacht werden. Erfahren Sie, wie Sie diese Fehler erkennen und wie Sie gegen sie vorgehen.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdec41d2d058a48153d6126fea534c1efaf16e16ccabef5d5e940daa73e839a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048948"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Behandeln von Fehlern bei der Signatur von App-Paketen

Ein Fehler bei der App-Bereitstellung kann durch einen Fehler beim Überprüfen der digitalen Signatur des App-Pakets verursacht werden. Erfahren Sie, wie Sie diese Fehler erkennen und wie Sie gegen sie vorgehen.

Wenn Sie eine gepackte Windows App bereitstellen, versucht Windows immer, die digitale Signatur für das App-Paket zu überprüfen. Fehler während der Signaturvalidierung blockieren die Bereitstellung des Pakets. Aber warum das Paket nicht überprüft wurde, ist möglicherweise nicht offensichtlich. Insbesondere wenn Sie Ihre Pakete mit privaten Zertifikaten für lokale Tests signieren, müssen Sie häufig auch die Vertrauensstellung für diese Zertifikate verwalten. Eine falsche Konfiguration der Zertifikatvertrauensstellung kann zu Fehlern bei der Signaturüberprüfung führen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Verpacken, Bereitstellen und Abfragen von Windows-Apps](appx-portal.md)
-   [Überprüfung der Zertifikatvertrauensstellung](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Voraussetzungen

-   [Windows Ereignisprotokoll,](/windows/desktop/WES/windows-event-log) um Installationsfehler zu diagnostizieren.
-   [Certutil-Aufgaben zum Verwalten von Zertifikaten](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) für die Manipulation des Zertifikatspeichers während der Problembehandlung

## <a name="instructions"></a>Anweisungen

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Schritt 1: Untersuchen von Ereignisprotokollen auf Diagnoseinformationen

Je nachdem, wie Sie versucht haben, Ihre App bereitzustellen, haben Sie möglicherweise keinen aussagekräftigen Fehlercode für den Bereitstellungsfehler erhalten. In diesem Fall können Sie den Fehlercode in der Regel direkt aus den Ereignisprotokollen abrufen.

**So erhalten Sie den Fehlercode aus den Ereignisprotokollen**

1.  Führen Sie **eventvwr.msc aus.**
2.  Wechseln Sie zu **Ereignisanzeige (lokal)**  >  **Anwendungs- und Dienstprotokolle**  >  **Microsoft**  >  **Windows**.
3.  Das erste zu überprüfende Protokoll ist **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**.
4.  Bereitstellungsbezogene Fehler werden in **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational** aufgezeichnet.

    Suchen Sie bei Bereitstellungsfehlern nach dem letzten Fehlerereignis 404. Dieses Fehlerereignis enthält den Fehlercode und eine Beschreibung, warum die Bereitstellung fehlgeschlagen ist. Wenn dem Ereignis 404 ein Fehlerereignis 465 vorangestellt wurde, liegt ein Problem beim Öffnen des Pakets vor.

Wenn der Fehler 465 nicht aufgetreten ist, finden Sie weitere Informationen unter Allgemeine [Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps.](troubleshooting.md) Andernfalls finden Sie in dieser Tabelle allgemeine Fehlercodes, die in der Fehlerzeichenfolge für das Fehlerereignis 465 angezeigt werden können:

| Fehlercode | Fehler                                 | BESCHREIBUNG                                                                                                          | Vorschlag                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | FEHLER \_ BEIM INSTALLIEREN DES \_ \_ GEÖFFNETEN PAKETS \_ | Das App-Paket konnte nicht geöffnet werden.                                                                                 | Dieser Fehler weist in der Regel auf ein Problem mit dem Paket hin. Sie müssen das Paket erneut erstellen und signieren. Weitere Informationen finden Sie unter [Verwenden von App Packager.](make-appx-package--makeappx-exe-.md) |
| 0x80080205 | APPX \_ E \_ INVALID \_ BLOCKMAP            | Das App-Paket wurde manipuliert oder weist eine ungültige Blockzuordnung auf.                                                  | Das Paket ist beschädigt. Sie müssen das Paket erneut erstellen und signieren. Weitere Informationen finden Sie unter [Verwenden von App Packager.](make-appx-package--makeappx-exe-.md)                                  |
| 0x800B0004 | \_ \_ E-BETREFF VERTRAUEN NICHT \_ \_ VERTRAUENSWÜRDIG       | Das App-Paket wurde manipuliert.                                                                              | Der Paketinhalt stimmt nicht mehr mit seiner digitalen Signatur überein. Sie müssen das Paket erneut signieren. Weitere Informationen finden Sie unter [Signieren eines App-Pakets mit SignTool.](how-to-sign-a-package-using-signtool.md)  |
| 0x800B0100 | TRUST \_ E \_ NOSIGNATURE                 | Das App-Paket ist nicht signiert.                                                                                         | Nur signierte Windows App-Pakete können bereitgestellt werden. Informationen zum Signieren eines App-Pakets finden Sie unter [Signieren eines App-Pakets mit SignTool.](how-to-sign-a-package-using-signtool.md)                  |
| 0x800B0109 | CERT \_ E \_ UNTRUSTED \_ ROOT              | Die Zertifikatkette, die zum Signieren des App-Pakets verwendet wurde, endet mit einem Stammzertifikat, das nicht vertrauenswürdig ist.           | Fahren Sie mit Schritt 2 fort, um probleme mit der Zertifikatvertrauensstellung zu beheben.                                                                                                                                                  |
| 0x800B010A | \_ \_ ZERTIFIKAT-E-VERKETTUNG                     | Es konnte keine Zertifikatkette für eine vertrauenswürdige Stammzertifizierungsstelle aus dem Zertifikat erstellt werden, das zum Signieren des App-Pakets verwendet wurde. | Fahren Sie mit Schritt 2 fort, um probleme mit der Zertifikatvertrauensstellung zu beheben.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Schritt 2: Bestimmen der Zertifikatkette, die zum Signieren des App-Pakets verwendet wird

Um die Zertifikate zu finden, denen der lokale Computer vertrauen muss, können Sie die Zertifikatkette für die digitale Signatur im App-Paket untersuchen.

**So bestimmen Sie die Zertifikatkette**

1.  Klicken Sie im Datei-Explorer mit der rechten Maustaste auf das App-Paket, und wählen Sie **Eigenschaften** aus.
2.  Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Digitale Signaturen aus,** auf der auch angezeigt wird, ob die Signatur überprüft werden kann.
3.  Wählen Sie in der Liste Signatur die Signatur aus, und klicken Sie dann auf die Schaltfläche **Details.**
4.  Klicken Sie im Dialogfeld Details zur **digitalen Signatur** auf die Schaltfläche **Zertifikat anzeigen.**
5.  Wählen Sie im Dialogfeld Zertifikat die Registerkarte **Zertifizierungspfad** aus. 

Das oberste Zertifikat in der Kette ist das Stammzertifikat, und das untere Zertifikat ist das Signaturzertifikat. Wenn sich nur ein einzelnes Zertifikat in der Kette befindet, ist das Signaturzertifikat auch ein eigenes Stammzertifikat. Sie können die Seriennummer für jedes Zertifikat bestimmen, das Sie dann mit [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))verwenden:

**So bestimmen Sie die Seriennummer für jedes Zertifikat**

1.  Wählen Sie im Bereich Zertifizierungspfad das Zertifikat aus, und klicken Sie dann auf **Zertifikat anzeigen.**
2.  Wählen Sie im Dialogfeld Zertifikat die Registerkarte **Details** aus, auf der die Seriennummer und andere nützliche Eigenschaften des Zertifikats angezeigt werden.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Schritt 3: Bestimmen der Zertifikate, die vom lokalen Computer als vertrauenswürdig eingestuft werden

Um ein App-Paket bereitstellen zu können, muss es nicht nur im Kontext des Benutzers, sondern auch im Kontext des lokalen Computers als vertrauenswürdig eingestuft werden. Daher kann die digitale Signatur gültig sein, wenn sie im vorherigen Schritt auf der Registerkarte Digitale Signaturen angezeigt wird. Die Überprüfung während der Bereitstellung des App-Pakets schlägt jedoch fehl.

**So bestimmen Sie, ob die Zertifikatkette, die zum Signieren des App-Pakets verwendet wird, vom lokalen Computer ausdrücklich als vertrauenswürdig eingestuft wird**

1.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Wenn Sie die Seriennummer des Zertifikats nicht angeben, [listet Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) alle Zertifikate auf, die vom lokalen Computer für diesen Speicher als vertrauenswürdig eingestuft werden.

Das Paket kann aufgrund von Zertifikatverkettungsfehlern möglicherweise nicht installiert werden, auch wenn das Signaturzertifikat nicht selbstsigniert ist und sich das Stammzertifikat im Stammspeicher des lokalen Computers befindet. In diesem Fall kann ein Problem mit der Vertrauensstellung für die Zwischenzertifizierungsstellen vorliegen. Weitere Informationen zu diesem Problem finden Sie unter [Arbeiten mit Zertifikaten.](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85))

## <a name="remarks"></a>Hinweise

Wenn Sie festgestellt haben, dass das Paket nicht bereitgestellt werden konnte, weil das Signaturzertifikat nicht vertrauenswürdig ist, installieren Sie das Paket nur, wenn Sie wissen, woher es stammt und Sie ihm vertrauen.

Wenn Sie der App für die Installation manuell vertrauen möchten (z. B. zum Installieren Ihres eigenen testsignten App-Pakets), können Sie das Zertifikat manuell der Zertifikatvertrauensstellung des lokalen Computers aus dem App-Paket hinzufügen.

**So fügen Sie das Zertifikat der Zertifikatvertrauensstellung auf dem lokalen Computer manuell hinzu**

1.  Klicken Sie im Datei-Explorer mit der rechten Maustaste auf das App-Paket, und wählen Sie im Kontextmenü des **Popupmenüs Eigenschaften** aus.
2.  Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Digitale Signaturen** aus.
3.  Wählen Sie in der Liste Signatur die Signatur aus, und klicken Sie dann auf die Schaltfläche **Details.**
4.  Klicken Sie im Dialogfeld Details zur **digitalen Signatur** auf die Schaltfläche **Zertifikat anzeigen.**
5.  Klicken Sie im Dialogfeld **Zertifikat** auf Das **Zertifikat installieren...** Schaltfläche.
6.  Wählen Sie im Zertifikatimport-Assistenten die Option **Lokaler Computer aus,** und klicken Sie dann auf **Weiter.** Sie müssen Administratorrechte erteilen, um den Fortfahren zu ermöglichen.
7.  Wählen **Sie Alle Zertifikate im folgenden Speicher speichern aus, und** navigieren Sie zum Speicher **Vertrauenswürdige** Personen.
8.  Klicken **Sie auf Weiter** und dann auf Fertig **stellen,** um den Assistenten abzuschließen.

Nach diesem manuellen Hinzufügen können Sie sehen, dass das Zertifikat jetzt im Dialogfeld Zertifikat **als vertrauenswürdig eingestuft** wird.

Sie können das Zertifikat entfernen, nachdem Sie es nicht mehr benötigen.

**So entfernen Sie das Zertifikat**

1.  Führen **Cmd.exe** als Administrator aus.
2.  Führen Sie an der Administratorbefehlsaufforderung den folgenden Befehl aus:

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Suchen Sie nach der Seriennummer des Zertifikats, das Sie installiert haben. Diese Zahl ist die *certID.*
4.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

Es wird empfohlen, das manuelle Hinzufügen von Stammzertifikaten zum lokalen Computer Vertrauenswürdige Stammzertifizierungsstellen Zertifikatszertifikats [Store.](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store) Mehrere Anwendungen, die mit Zertifikaten signiert sind, die mit demselben Stammzertifikat verkettet sind, z. B. Unternehmensanwendungen, können effizienter sein als die Installation einzelner Zertifikate im Speicher für vertrauenswürdige Personen. Der Speicher für vertrauenswürdige Personen enthält Zertifikate, die standardmäßig als vertrauenswürdig angesehen werden und daher nicht von höheren Zertifizierungsstellen oder Zertifikatvertrauenslisten oder -ketten überprüft werden. Überlegungen zum Hinzufügen von Zertifikaten zum zertifikatbasierten Vertrauenswürdige Stammzertifizierungsstellen finden Sie unter Bewährte Methoden für die [Codesignatur.](/previous-versions/windows/hardware/design/dn653556(v=vs.85))

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Durch das Hinzufügen eines Zertifikats [zu zertifikatspeichern](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)auf dem lokalen Computer wirken Sie sich auf die Zertifikatvertrauensstellung aller Benutzer auf dem Computer aus. Es wird empfohlen, alle Codesignaturzertifikate, die Sie zum Testen von App-Paketen wünschen, im Zertifikatspeicher für vertrauenswürdige Personen zu installieren. Entfernen Sie diese Zertifikate umgehend, wenn sie nicht mehr benötigt werden, um zu verhindern, dass sie verwendet werden, um die Systemvertrauensstellung zu gefährden. Wenn Sie eigene Testzertifikate zum Signieren von App-Paketen erstellen, wird auch empfohlen, die Berechtigungen einzuschränken, die dem Testzertifikat zugeordnet sind. Informationen zum Erstellen von Testzertifikaten zum Signieren von App-Paketen finden Sie unter Erstellen eines [App-Paketsignaturzertifikats.](how-to-create-a-package-signing-certificate.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Beispiele**
</dt> <dt>

[Beispiel zum Erstellen eines App-Pakets](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Konzepte**
</dt> <dt>

[Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps](troubleshooting.md)
</dt> <dt>

[Certutil-Aufgaben zum Verwalten von Zertifikaten](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 
