---
title: Problembehandlung bei App-Paket Signatur Fehlern
description: Ein Fehler bei der APP-Bereitstellung kann durch einen Fehler bei der Überprüfung der digitalen Signatur des App-Pakets verursacht werden. Erfahren Sie, wie Sie diese Fehler erkennen und wie Sie damit zu tun haben.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6f50dc5ff428e74f4928fc20775b13de7c3be9
ms.sourcegitcommit: 784b5954a1646e2406cd4ee27a9e4f50e28ee9b7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106374831"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Problembehandlung bei App-Paket Signatur Fehlern

Ein Fehler bei der APP-Bereitstellung kann durch einen Fehler bei der Überprüfung der digitalen Signatur des App-Pakets verursacht werden. Erfahren Sie, wie Sie diese Fehler erkennen und wie Sie damit zu tun haben.

Beim Bereitstellen einer APP mit Windows-App-Paketen wird von Windows immer versucht, die digitale Signatur im App-Paket zu überprüfen. Fehler während der Überprüfung der Signatur Überprüfung Blockieren des Pakets. Aber warum das Paket nicht validiert wurde, ist möglicherweise nicht offensichtlich. Insbesondere, wenn Sie Ihre Pakete mit privaten Zertifikaten für lokale Tests signieren, müssen Sie häufig auch die Vertrauenswürdigkeit für diese Zertifikate verwalten. Eine falsche Konfiguration der Zertifikat Vertrauensstellung kann zu Fehlern bei der Signatur Überprüfung führen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Verpacken, Bereitstellung und Abfrage von Windows-apps](appx-portal.md)
-   [Zertifikat Vertrauensstellungs Überprüfung](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Voraussetzungen

-   [Windows-Ereignisprotokoll](/windows/desktop/WES/windows-event-log) zur Diagnose von Installationsfehlern.
-   [Certutil-Aufgaben zum Verwalten von Zertifikaten](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) für die Zertifikat Speicher Bearbeitung während der Problembehandlung

## <a name="instructions"></a>Anweisungen

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Schritt 1: Untersuchen der Ereignisprotokolle nach Diagnoseinformationen

Je nachdem, wie Sie versuchen, die APP bereitzustellen, haben Sie möglicherweise keinen sinnvollen Fehlercode für den Bereitstellungs Fehler erhalten. In diesem Fall können Sie den Fehlercode in der Regel direkt aus den Ereignisprotokollen erhalten.

**So erhalten Sie den Fehlercode aus den Ereignisprotokollen**

1.  Führen Sie **eventvwr. msc** aus.
2.  Wechseln Sie zu **Ereignisanzeige (local)**  >  **Anwendungs-und Dienst Protokolle**  >  **Microsoft**  >  **Windows**.
3.  Das erste zu überprüfen Protokoll lautet **appxpackagingom**  >  **Microsoft-Windows-appxpackaging/Operational**.
4.  Bereitstellungs bezogene Fehler werden in **appxdeployment-Server**  >  **Microsoft-Windows-appxdeploymentserver/Operational** aufgezeichnet.

    Suchen Sie bei Bereitstellungs Fehlern nach dem letzten Fehler Ereignis 404. Dieses Ereignis vom Typ Fehler enthält den Fehlercode und eine Beschreibung, warum die Bereitstellung fehlgeschlagen ist. Wenn ein Fehler Ereignis 465 dem Ereignis 404 vorangestellt war, gab es ein Problem beim Öffnen des Pakets.

Wenn der Fehler 465 nicht aufgetreten ist, lesen Sie allgemeine Problembehandlung bei der [Paket Erstellung, Bereitstellung und Abfrage von Windows-apps](troubleshooting.md). Andernfalls finden Sie in dieser Tabelle allgemeine Fehlercodes, die in der Fehler Zeichenfolge für Fehler Ereignis 465 angezeigt werden können:

| Fehlercode | Fehler                                 | BESCHREIBUNG                                                                                                          | Vorschlag                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | Fehler beim \_ Installieren des \_ geöffneten \_ Pakets \_ | Das App-Paket konnte nicht geöffnet werden.                                                                                 | Dieser Fehler weist in der Regel auf ein Problem mit dem Paket hin. Sie müssen das Paket erneut erstellen und signieren. Weitere Informationen finden Sie unter [Verwenden von App Packager](make-appx-package--makeappx-exe-.md). |
| 0x80080205 | AppX \_ E \_ ungültige \_ blockmap            | Das App-Paket wurde manipuliert oder weist eine ungültige Block Zuordnung auf.                                                  | Das Paket ist beschädigt. Sie müssen das Paket erneut erstellen und signieren. Weitere Informationen finden Sie unter [Verwenden von App Packager](make-appx-package--makeappx-exe-.md).                                  |
| 0x800b0004 | Vertrauens \_ würdiger E- \_ Betreff \_ nicht \_ vertrauenswürdig       | Das App-Paket wurde manipuliert.                                                                              | Der Paket Inhalt stimmt nicht mehr mit der digitalen Signatur des Pakets. Sie müssen das Paket erneut signieren. Weitere Informationen finden Sie unter [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md).  |
| 0x800B0100 | \_e \_ NoSignature Vertrauen                 | Das App-Paket ist nicht signiert.                                                                                         | Es können nur signierte Windows-App-Pakete bereitgestellt werden. Informationen zum Signieren eines App-Pakets finden [Sie unter Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md).                  |
| 0x800B0109 | CERT \_ E \_ nicht vertrauenswürdiger Stamm \_              | Die Zertifikat Kette, die zum Signieren des App-Pakets verwendet wurde, endet in einem Stamm Zertifikat, das nicht vertrauenswürdig ist.           | Fahren Sie mit Schritt 2 fort, um die Zertifikats Vertrauensstellung zu beheben.                                                                                                                                                  |
| 0x800b010a | Zertifikat- \_ E- \_ Verkettung                     | Es konnte keine Zertifikat Kette für eine vertrauenswürdige Stamm Zertifizierungsstelle aus dem Zertifikat erstellt werden, das zum Signieren des App-Pakets verwendet wurde. | Fahren Sie mit Schritt 2 fort, um die Zertifikats Vertrauensstellung zu beheben.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Schritt 2: Bestimmen der zum Signieren des App-Pakets verwendeten Zertifikat Kette

Zum Ermitteln der Zertifikate, denen der lokale Computer vertrauen muss, können Sie die Zertifikat Kette für die digitale Signatur im App-Paket überprüfen.

**So bestimmen Sie die Zertifikat Kette**

1.  Klicken Sie im Datei-Explorer mit der rechten Maustaste auf das App-Paket, und wählen Sie **Eigenschaften** aus.
2.  Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **digitale Signaturen** aus, auf der auch angezeigt wird, ob die Signatur überprüft werden kann.
3.  Wählen Sie in der Liste Signatur die Signatur aus, und klicken Sie dann auf die Schaltfläche **Details** .
4.  Klicken Sie im Dialogfeld " **digitale Signatur Details** " auf die Schaltfläche " **Zertifikat anzeigen** ".
5.  Klicken Sie im Dialogfeld **Zertifikat** auf die Registerkarte **Zertifizierungspfad** .

Das oberste Zertifikat in der Kette ist das Stamm Zertifikat, und das untere Zertifikat ist das Signaturzertifikat. Wenn sich nur ein einzelnes Zertifikat in der Kette befindet, ist das Signaturzertifikat auch sein eigenes Stamm Zertifikat. Sie können die Seriennummer für jedes Zertifikat ermitteln, das Sie dann mit [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))verwenden:

**So bestimmen Sie die Seriennummer für jedes Zertifikat**

1.  Wählen Sie im Bereich "Zertifizierungspfad" das Zertifikat aus, und klicken Sie dann auf **Zertifikat anzeigen**.
2.  Klicken Sie im Dialogfeld Zertifikat auf die Registerkarte **Details** , auf der die Seriennummer und andere nützliche Eigenschaften des Zertifikats angezeigt werden.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Schritt 3: Bestimmen der Zertifikate, die vom lokalen Computer als vertrauenswürdig eingestuft werden

Damit ein App-Paket bereitgestellt werden kann, darf es nicht nur im Kontext des Benutzers, sondern auch im Kontext des lokalen Computers als vertrauenswürdig eingestuft werden. Folglich kann die digitale Signatur gültig sein, wenn Sie im vorherigen Schritt auf der Registerkarte Digitale Signaturen angezeigt wird, die Überprüfung während der Bereitstellung des App-Pakets jedoch weiterhin fehlschlägt.

**So bestimmen Sie, ob die Zertifikat Kette, die zum Signieren des App-Pakets verwendet wird, vom lokalen Computer**

1.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Wenn Sie die Seriennummer des Zertifikats nicht angeben, listet [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) alle Zertifikate auf, die vom lokalen Computer für diesen Speicher als vertrauenswürdig eingestuft werden.

Das Paket kann aufgrund von Fehlern bei der Zertifikat Verkettung möglicherweise nicht installiert werden, auch wenn das Signaturzertifikat nicht selbst signiert ist und sich das Stamm Zertifikat im Stamm Speicher des lokalen Computers befindet. In diesem Fall liegt möglicherweise ein Problem mit der Vertrauensstellung für die zwischen Zertifizierungsstellen vor. Weitere Informationen zu diesem Problem finden Sie unter [Arbeiten mit Zertifikaten](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Bemerkungen

Wenn Sie festgestellt haben, dass das Paket nicht bereitgestellt werden konnte, weil das Signaturzertifikat nicht vertrauenswürdig ist, installieren Sie das Paket nur, wenn Sie wissen, woher es stammt, und vertrauenswürdig

Wenn Sie die APP manuell für die Installation (z. b. zum Installieren eines eigenen Test signierten App-Pakets) als vertrauenswürdig einstufen möchten, können Sie das Zertifikat manuell aus dem App-Paket der Zertifikat Vertrauensstellung des lokalen Computers hinzufügen.

**So fügen Sie das Zertifikat manuell der Zertifikat Vertrauensstellung des lokalen Computers hinzu**

1.  Klicken Sie im Datei-Explorer mit der rechten Maustaste auf das App-Paket, und wählen Sie im Popup Kontextmenü **Eigenschaften** aus.
2.  Klicken Sie im Dialogfeld **Eigenschaften** auf die Registerkarte **digitale Signaturen** .
3.  Wählen Sie in der Liste Signatur die Signatur aus, und klicken Sie dann auf die Schaltfläche **Details** .
4.  Klicken Sie im Dialogfeld " **digitale Signatur Details** " auf die Schaltfläche " **Zertifikat anzeigen** ".
5.  Klicken Sie im Dialogfeld **Zertifikat** auf **Zertifikat installieren...** .
6.  Wählen Sie im Zertifikat Import-Assistenten die Option **lokaler Computer** aus, und klicken Sie dann auf **weiter**. Zum Fortfahren müssen Sie Administratorrechte erteilen.
7.  Wählen Sie **alle Zertifikate in folgendem Speicher speichern aus** , und navigieren Sie zum Speicher für **Vertrauenswürdige Personen** .
8.  Klicken Sie auf **weiter** und dann auf **Fertig** stellen, um den Assistenten abzuschließen.

Nach diesem manuellen hinzufügen können Sie sehen, dass das Zertifikat im Dialogfeld **Zertifikat** vertrauenswürdig ist.

Sie können das Zertifikat entfernen, wenn es nicht mehr benötigt wird.

**So entfernen Sie das Zertifikat**

1.  Führen Sie **Cmd.exe** als Administrator aus.
2.  Führen Sie an der Administrator Eingabeaufforderung den folgenden Befehl aus:

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Suchen Sie nach der Seriennummer des Zertifikats, das Sie installiert haben. Diese Zahl ist die *CertID*.
4.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

Es wird empfohlen, dass Sie dem [Zertifikat Speicher für vertrauenswürdige Stamm Zertifizierungs](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)Stellen des lokalen Computers keine Stamm Zertifikate manuell hinzufügen. Mehrere Anwendungen, die mit Zertifikaten signiert sind, die mit demselben Stamm Zertifikat verkettet sind (z. b. Branchen Anwendungen), können effizienter sein als die Installation einzelner Zertifikate im Speicher für vertrauenswürdige Personen. Der Speicher für vertrauenswürdige Personen enthält Zertifikate, die standardmäßig als vertrauenswürdig eingestuft werden und daher nicht von höheren Autoritäten oder Zertifikat Vertrauens Listen oder-Ketten überprüft werden. Überlegungen zum Hinzufügen von Zertifikaten zum Zertifikat Speicher für vertrauenswürdige Stamm Zertifizierungsstellen finden Sie unter [bewährte Methoden für die Code Signatur](/previous-versions/windows/hardware/design/dn653556(v=vs.85)).

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Wenn Sie einem Zertifikat [Speicher des lokalen](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)Computers ein Zertifikat hinzufügen, haben Sie Auswirkungen auf die Zertifikats Vertrauensstellung aller Benutzer auf dem Computer. Es wird empfohlen, dass Sie alle Code Signatur Zertifikate installieren, die Sie zum Testen von App-Paketen im Zertifikat Speicher für vertrauenswürdige Personen benötigen. Entfernen Sie diese Zertifikate unverzüglich, wenn Sie nicht mehr benötigt werden, um zu verhindern, dass Sie zur Gefährdung der System Vertrauensstellung verwendet werden. Wenn Sie eigene Test Zertifikate zum Signieren von App-Paketen erstellen, empfiehlt es sich auch, die dem Test Zertifikat zugeordneten Berechtigungen einzuschränken. Informationen zum Erstellen von Test Zertifikaten zum Signieren von App-Paketen finden [Sie unter Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Beispiele**
</dt> <dt>

[App-Paket erstellen (Beispiel)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Konzepte**
</dt> <dt>

[Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps](troubleshooting.md)
</dt> <dt>

[Certutil-Aufgaben für die Verwaltung von Zertifikaten](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 
