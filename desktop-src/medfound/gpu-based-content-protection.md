---
description: Beschreibt Videoinhalte&\# 8211;Schutzfunktionen, die ein Grafiktreiber bereitstellen kann.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based Content Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e09829984273c35524fe9c8f3cd19e759e18dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465037"
---
# <a name="gpu-based-content-protection"></a>GPU-Based Content Protection

In diesem Thema werden Funktionen zum Schutz von Videoinhalten beschrieben, die ein Grafiktreiber bereitstellen kann.

-   [Introduction (Einführung)](#introduction)
-   [Übersicht über den Decodierungsprozess](#overview-of-the-decoding-process)
-   [Verschlüsseln komprimierter Videopuffer für den Decoder](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. Abfragen der Content Protection Funktionen des Treibers](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Konfigurieren des authentifizierten Kanals](#2-configure-the-authenticated-channel)
    -   [3. Konfigurieren der Kryptografiesitzung](#3-configure-the-cryptographic-session)
    -   [4. Abrufen eines Handles für das DXVA-Decodergerät](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. Zuordnen des DXVA-Decoders zur Kryptografiesitzung](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Senden von Befehlen für authentifizierte Kanäle](#sending-authenticated-channel-commands)
-   [Senden authentifizierter Kanalabfragen](#sending-authenticated-channel-queries)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das folgende Diagramm zeigt eine vereinfachte Ansicht der Art und Weise, wie geschützte Videoinhalte die zu rendernde Pipeline durchlaufen.

![Ein Diagramm, das geschützte Videoinhalte zeigt.](images/d3d9video01.png)

> [!Note]  
> Der Geschützte Medienpfad (Protected [Media Path,](protected-media-path.md) PMP) ist in diesem Diagramm nicht dargestellt. Der hier gezeigte Datenfluss kann innerhalb eines PMP-Prozesses oder in einem Anwendungsprozess auftreten.

 

Der Decoder empfängt verschlüsselte, komprimierte Videodaten aus einer externen Quelle. Es wird davon ausgegangen, dass der Decoder auch einen kryptografischen Schlüssel erhält, um diese Daten zu entschlüsseln. In diesem Thema wird der Schlüsselaustausch zwischen der Videoquelle und dem Decoder nicht beschrieben, aber PMP definiert einen möglichen Mechanismus. Die GPU ist in dieser Phase nicht beteiligt.

Für die hardwarebeschleunigte Decodierung übergibt der Softwaredecoder komprimierte Videoinhalte an die GPU. Um diesen Inhalt zu schützen, verschlüsselt der Decoder die Daten erneut, in der Regel mithilfe von AES-CTR, bevor er sie an die Hardwarebeschleunigung übergibt. Zwischen dem Decoder und dem Grafiktreiber wird ein Schlüsselaustauschmechanismus definiert.

Decodierte Videoframes werden im Videospeicher gespeichert, in der Regel im Klartext. An diesem Punkt werden die Frames verarbeitet und dann dargestellt. Es gibt zwei Hauptoptionen für die Präsentation.

-   Frames können mithilfe einer Hardwareüberlagerung dargestellt werden. Weitere Informationen finden Sie unter [Hardwareüberlagerungsunterstützung.](hardware-overlay-support.md)
-   Frames können von der Desktopfensterverwaltung (DESKTOP Window Manage, DWM) mithilfe einer freigegebenen Oberfläche dargestellt werden.

Der letzte Schritt besteht darin, den Frame auf dem Monitor anzuzeigen, der möglicherweise einen Linkschutz zwischen der Grafikkarte und dem Anzeigegerät erfordert. Ein Beispiel für den Linkschutz ist High-Bandwidth Digital Content Protection (HDCP). Der Linkschutz wird mit dem [Output Protection Manager](output-protection-manager.md) (OPM) konfiguriert. In diesem Thema wird OPM nicht beschrieben. Weitere Informationen finden Sie unter [Verwenden von Output Protection Manager.](using-output-protection-manager.md)

## <a name="overview-of-the-decoding-process"></a>Übersicht über den Decodierungsprozess

Während der hardwarebeschleunigten Decodierung muss der Softwaredecoder komprimierte Videodaten an die Grafikkarte übergeben. Bei Premium-Inhalten müssen diese Daten in der Regel mit verschlüsselung mit symmetrischem Schlüssel verschlüsselt werden, bevor sie an die GPU gesendet werden.

Zum Verschlüsseln des Videos für die Decodierung verwendet der Softwaredecoder die folgenden Schnittstellen:

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Stellt das DXVA-Decodergerät dar, das auch als Accelerator bezeichnet wird.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Stellt eine kryptografische Sitzung dar, die den Verschlüsselungsschlüssel bereitstellt.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Stellt einen authentifizierten Kanal dar, der es dem Softwaredecoder ermöglicht, die kryptografische Sitzung dem DXVA-Decoder zuzuordnen.

![Ein Diagramm, das die Direct3d9-Decodierungsschnittstellen zeigt.](images/d3d9video02.png)

Alle diese Schnittstellen werden wie folgt vom Direct3D-Gerät abgerufen:



| Schnittstelle                                                                | Erstellung                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Rufen Sie [**IDirectXVideoDecoderService::CreateVideoDecoder auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder) Das DXVA-Decodergerät wird durch eine DXVA-Profil-GUID identifiziert. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Rufen Sie [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession)auf.                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Rufen Sie [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)auf.                                                           |



 

> [!Note]  
> Rufen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf einem D3D9Ex-Gerät auf, um einen Zeiger auf die [**IDirect3DDevice9Video-Schnittstelle**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) abzurufen.

 

Der authentifizierte Kanal stellt einen vertrauenswürdigen Kommunikationskanal zwischen dem Softwaredecoder und dem Treiber bereit. Der Kommunikationskanal funktioniert wie folgt:

-   Der Treiber stellt eine X.509-Zertifikatkette bereit, deren Stammzertifikat von Microsoft signiert wurde.
-   Das Zertifikat enthält einen öffentlichen RSA-Schlüssel für den Treiber.
-   Der Softwaredecoder verwendet den öffentlichen Schlüssel, um dem Treiber einen 128-Bit-AES-Sitzungsschlüssel zu senden.
-   Der Softwaredecoder sendet Abfragen und Befehle an den authentifizierten Kanal.
-   Der Sitzungsschlüssel wird verwendet, um Nachrichtenauthentifizierungscodes (Message Authentication Codes, MACs) für die Abfragen und Befehle zu berechnen. Der Treiber verwendet die MACs, um die Integrität der Abfrage-/Befehlsdaten zu überprüfen, und der Softwaredecoder verwendet sie, um die Integrität der Antwortdaten des Treibers zu überprüfen.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Verschlüsseln komprimierter Videopuffer für den Decoder

Hier finden Sie eine allgemeine Übersicht über den Verschlüsselungs- und Decodierungsprozess:

1.  Der Softwaredecoder empfängt einen Stream verschlüsselter Daten aus der Videoquelle. Der Decoder entschlüsselt diesen Stream.
2.  Der Softwaredecoder handelt einen Sitzungsschlüssel mit der kryptografischen Sitzung aus.
3.  Der Softwaredecoder verwendet den authentifizierten Kanal, um die kryptografische Sitzung dem DXVA-Decodergerät zuzuordnen.
4.  Der Softwaredecoder fügt komprimierte Daten in DXVA-Puffer ein, die er vom DXVA-Decodergerät (Accelerator) erhält. Bei geschützten Inhalten verschlüsselt der Softwareencoder die Daten, die in die DXVA-Puffer abgelegt werden, mithilfe des Sitzungsschlüssels für die Verschlüsselung.
    > [!Note]  
    > Einige Treiber verwenden einen Inhaltsschlüssel anstelle des Sitzungsschlüssels für die Verschlüsselung. Der Inhaltsschlüssel kann sich von einem Frame zum nächsten ändern.

     

5.  Der Decoder sendet die verschlüsselten komprimierten Puffer an die Zugriffstaste. Bei AES-CTR übergibt der Decoder auch den Initialisierungsvektor. Wenn ein Inhaltsschlüssel verwendet wird, übergibt der Decoder den Inhaltsschlüssel, der mit dem Sitzungsschlüssel verschlüsselt wurde.

Direct3D verfügt über Standardunterstützung für 128-Bit-AES-CTR, ist aber für die Erweiterung auf zusätzliche Verschlüsselungstypen konzipiert.

Die nächsten fünf Abschnitte enthalten ausführlichere Schritte.

-   [1. Abfragen der Content Protection Funktionen des Treibers](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Konfigurieren des authentifizierten Kanals](#2-configure-the-authenticated-channel)
-   [3. Konfigurieren der Kryptografiesitzung](#3-configure-the-cryptographic-session)
-   [4. Abrufen eines Handles für das DXVA-Decodergerät](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. Zuordnen des DXVA-Decoders zur Kryptografiesitzung](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. Abfragen der Content Protection Funktionen des Treibers

Bevor Sie versuchen, die Verschlüsselung anzuwenden, erhalten Sie die Inhaltsschutzfunktionen des Treibers.

1.  Abrufen eines Zeigers auf das Direct3D 9-Gerät.
2.  Rufen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die [**IDirect3DDevice9Video-Schnittstelle**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) auf.
3.  Rufen Sie [**IDirect3DDevice9Video::GetContentProtectionCaps auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps) Diese Methode füllt eine [**D3DCONTENTPROTECTIONCAPS-Struktur**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) mit den Inhaltsschutzfunktionen des Treibers aus.

Suchen Sie insbesondere nach den folgenden Funktionen:

-   Wenn das **Caps-Element** das **flag D3DCPCAPS_SOFTWARE** oder **D3DCPCAPS_HARDWARE** enthält, kann der Treiber die Verschlüsselung durchführen.
-   Das **KeyExchangeType-Element** gibt an, wie der Schlüsselaustausch für den Sitzungsschlüssel ausgeführt wird.
-   Wenn der **Caps-Member** das **flag D3DCPCAPS_CONTENTKEY** enthält, verwendet der Treiber einen separaten Inhaltsschlüssel für die Verschlüsselung. Dies ist wichtig, wenn Sie den Sitzungsschlüssel generieren.

Zusätzliche Funktionen sind im **Caps-Member** angegeben.

### <a name="2-configure-the-authenticated-channel"></a>2. Konfigurieren des authentifizierten Kanals

Der nächste Schritt besteht darin, den authentifizierten Kanal zu konfigurieren.

1.  Rufen Sie [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) auf, um den authentifizierten Kanal zu erstellen. Geben Sie für den *ChannelType-Parameter* einen Kanaltyp an, der den Funktionen des Treibers entspricht.
    -   Der **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** Kanaltyp entspricht **D3DCPCAPS_SOFTWARE**.
    -   Der **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** Kanaltyp entspricht **D3DCPCAPS_HARDWARE**.

    Die **CreateAuthenticatedChannel-Methode** gibt einen Zeiger auf die [**IDirect3DAuthenticatedChannel9-Schnittstelle**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) zusammen mit einem Handle für den Kanal zurück. Das Handle wird später verwendet, um die kryptografische Sitzung dem authentifizierten Kanal zuzuordnen.
2.  Rufen Sie [**IDirect3DAuthenticatedChannel9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) auf, um die Größe des X.509-Zertifikats des Treibers abzurufen. Ordnen Sie einen Puffer der erforderlichen Größe zu.
3.  Rufen Sie [**IDirect3DAuthenticatedChannel9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) auf, um das Zertifikat abzurufen. Die -Methode kopiert das Zertifikat in den Puffer, der im vorherigen Schritt zugeordnet wurde.
4.  Vergewissern Sie sich, dass das Zertifikat des Treibers von Microsoft signiert und nicht widerrufen wurde.
5.  Abrufen des öffentlichen Schlüssels aus dem Zertifikat.
6.  Generieren Sie einen zufälligen RSA-Sitzungsschlüssel. Dieser Sitzungsschlüssel wird zum Signieren von Daten verwendet, die an den authentifizierten Kanal gesendet werden. Verschlüsseln Sie den Sitzungsschlüssel mit dem öffentlichen Schlüssel des Treibers.
7.  Rufen Sie [**IDirect3DAuthenticatedChannel9::NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) auf, um den verschlüsselten Sitzungsschlüssel an den Treiber zu senden.
8.  Initialisieren Sie den sicheren Kanal wie folgt:
    1.  Füllen Sie eine [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) Struktur aus, wie in der Dokumentation beschrieben.
    2.  Senden Sie den [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) Befehl, indem [**Sie IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) aufrufen, wie im Abschnitt [Senden von Befehlen](#sending-authenticated-channel-commands)für authentifizierte Kanäle beschrieben. Dieser Befehl enthält die Anfangssequenznummern für die Befehle und Abfragen, die an den authentifizierten Kanal gesendet werden.
9.  Überprüfen Sie den Kanaltyp, indem Sie eine [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) Abfrage an den authentifizierten Kanal senden, wie im Abschnitt Senden von Abfragen für [authentifizierte Kanäle](#sending-authenticated-channel-queries)beschrieben. Überprüfen Sie, ob der Kanaltyp mit dem übereinstimmt, den Sie in der [**CreateAuthenticatedChannel-Methode**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) angegeben haben.

### <a name="3-configure-the-cryptographic-session"></a>3. Konfigurieren der Kryptografiesitzung

Konfigurieren Sie als Nächstes die kryptografische Sitzung, und richten Sie den Sitzungsschlüssel ein.

1.  Rufen Sie [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) auf, um die kryptografische Sitzung zu erstellen. Diese Methode gibt einen Zeiger auf die [**IDirect3DCryptoSession9-Schnittstelle**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) und ein Handle für die kryptografische Sitzung zurück.
2.  Rufen Sie [**IDirect3DCryptoSession9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) auf, um die Größe des X.509-Zertifikats des Treibers abzurufen. Ordnen Sie einen Puffer der erforderlichen Größe zu.
3.  Rufen Sie [**IDirect3DCryptoSession9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) auf, um das Zertifikat abzurufen. Die -Methode kopiert das Zertifikat in den Puffer, der im vorherigen Schritt zugeordnet wurde.
4.  Vergewissern Sie sich, dass das Zertifikat des Treibers von Microsoft signiert und nicht widerrufen wurde.
5.  Abrufen des öffentlichen Schlüssels aus dem Zertifikat.
6.  Generieren Sie einen zufälligen RSA-Sitzungsschlüssel. Dies ist ein separater Sitzungsschlüssel vom Sitzungsschlüssel des authentifizierten Kanals. Verschlüsseln Sie den Sitzungsschlüssel mit dem öffentlichen Schlüssel des Treibers.
7.  Rufen Sie [**IDirect3DCryptoSession9::NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) auf, um den verschlüsselten Sitzungsschlüssel an den Treiber zu senden.
8.  Wenn die Inhaltsschutzfunktionen **D3DCPCAPS_CONTENTKEY** enthalten, erstellen Sie einen zufälligen RSA-Inhaltsschlüssel. Dies wird später im Decodierungsprozess verwendet.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. Abrufen eines Handles für das DXVA-Decodergerät

Für den nächsten Schritt benötigen Sie ein Handle für das DXVA-Decodergerät. Um dieses Handle zu erhalten, füllen Sie eine DXVA2_DecodeExecuteParams-Struktur wie folgt aus:


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



Legen Sie den **pExtensionData-Member** der [**DXVA2_DecodeExecuteParams-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) auf die Adresse einer [**DXVA2_DecodeExtensionData-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) fest.

Legen Sie in der [**DXVA2_DecodeExtensionData-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) den **Function-Member** auf **DXVA2_DECODE_GET_DRIVER_HANDLE** fest. Legen Sie **pPrivateOutputData** auf die Adresse eines Puffers fest, der groß genug ist, um einen **HANDLE-Wert** zu speichern. (Im vorherigen Beispiel ist dieser Puffer die Variable *hDecodeDeviceHandle.)*

Rufen Sie dann [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) auf, und übergeben Sie die Adresse der [**DXVA2_DecodeExecuteParams-Struktur.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) Das Handle für den DXVA-Decoder wird in **pPrivateOutputData** zurückgegeben.

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. Zuordnen des DXVA-Decoders zur Kryptografiesitzung

Ordnen Sie als Nächstes das DXVA-Decodergerät wie folgt dem Direct3D-Gerät und der kryptografischen Sitzung zu:

1.  Abrufen eines Handles für das DXVA-Decodergerät, wie im vorherigen Abschnitt beschrieben.
2.  Erhalten Sie ein Handle für das Direct3D-Gerät, indem Sie eine [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) Abfrage an den authentifizierten Kanal senden.
3.  Füllen Sie eine [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION-Struktur**](d3dauthenticatedchannel-configurecryptosession.md) mit den folgenden Informationen aus:
    -   Legen Sie den **DXVA2DecodeHandle-Member** auf das Handle des DXVA-Decodergeräts fest.
    -   Legen Sie das **CryptoSessionHandle-Element** auf das Handle für die kryptografische Sitzung fest. Dieses Handle wird von der [**IDirect3DDevice9Video::CreateCryptoSession-Methode**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) zurückgegeben.
    -   Legen Sie das **DeviceHandle-Element** auf das Direct3D-Gerätehandle fest.
4.  Rufen Sie [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) auf, um einen [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) Befehl an den authentifizierten Kanal zu senden.

Das folgende Diagramm veranschaulicht den Austausch von Handles:

![Ein Diagramm, das zeigt, wie der Dxva-Decoder der kryptografischen Sitzung zugeordnet ist.](images/d3d9video03.png)

Der Softwaredecoder kann jetzt den kryptografischen Sitzungsschlüssel verwenden, um die komprimierten Videopuffer zu verschlüsseln. Jeder komprimierte Puffer verfügt über einen eigenen Initialisierungsvektor (IV), der im **pvPVPState-Member** der [**DXVA2_DecodeBufferDesc-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) angegeben ist.

## <a name="sending-authenticated-channel-commands"></a>Senden von Befehlen für authentifizierte Kanäle

Eine Reihe von Befehlen wird zum Konfigurieren des authentifizierten Kanals und zum Festlegen verschiedener Inhaltsschutzfunktionen definiert. Eine Liste der Befehle finden Sie unter [Content Protection Befehle.](content-protection-commands.md)

Führen Sie die folgenden Schritte aus, um einen Befehl an den authentifizierten Kanal zu senden.

1.  Füllen Sie die Eingabedatenstruktur aus. Diese Datenstruktur ist immer eine [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) Struktur gefolgt von zusätzlichen Feldern. Füllen Sie die **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** Struktur wie in der folgenden Tabelle gezeigt aus.

    
| Member | BESCHREIBUNG | 
|--------|-------------|
| <strong>omac</strong> | Überspringen Sie dieses Feld vorerst. | 
| <strong>ConfigureType</strong> | GUID, die den Befehl identifiziert. Eine Liste der Befehle finden Sie unter <a href="content-protection-commands.md">Content Protection Befehle.</a> | 
| <strong>hChannel</strong> | Das Handle für den authentifizierten Kanal. | 
| <strong>SequenceNumber</strong> | Die Sequenznummer. Die erste Sequenznummer wird durch Senden eines <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> Befehls angegeben. Jedes Mal, wenn Sie einen anderen Befehl senden, erhöhen Sie diese Zahl um 1. Die Sequenznummer schützt vor Wiedergabeangriffen.    <blockquote>    [!Note]<br />    Es werden zwei separate Sequenznummern verwendet: eine für Befehle und eine für Abfragen.    </blockquote><br /><br /> | 


    

     

2.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **omac-Element** der Eingabestruktur angezeigt wird. Kopieren Sie dann diesen Tagwert in das **omac-Element.**
3.  Rufen Sie [**IDirect3DAuthenticatedChannel9::Configure auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
4.  Der Treiber platziert die Ausgabe des Befehls in der [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) Struktur.
5.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **omac-Member** der Ausgabestruktur angezeigt wird. Vergleichen Sie dies mit dem Wert des **omac-Elements.** Fehler, wenn sie nicht übereinstimmen.
6.  Vergleichen Sie die Werte der Member **ConfigureType,** **hChannel** und **SequenceNumber** in der Ausgabestruktur mit den Werten für diese Member. Fehler, wenn sie nicht übereinstimmen.
7.  Erhöhen Sie die Sequenznummer für den nächsten Befehl.

## <a name="sending-authenticated-channel-queries"></a>Senden authentifizierter Kanalabfragen

Für das Abrufen von Informationen über den authentifizierten Kanal wird eine Reihe von Abfragen definiert. Eine Liste der Abfragen finden Sie unter [Content Protection Abfragen.](content-protection-queries.md)

Führen Sie die folgenden Schritte aus, um einen Befehl an den authentifizierten Kanal zu senden.

1.  Füllen Sie die Eingabedatenstruktur aus. Diese Datenstruktur ist immer eine [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) Struktur, möglicherweise gefolgt von zusätzlichen Feldern. Füllen Sie die **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** Struktur wie in der folgenden Tabelle gezeigt aus.

    
| Member | BESCHREIBUNG | 
|--------|-------------|
| <strong>QueryType</strong> | GUID, die die Abfrage identifiziert. Eine Liste der Abfragen finden Sie unter <a href="content-protection-queries.md">Content Protection Abfragen.</a> | 
| <strong>hChannel</strong> | Das Handle für den authentifizierten Kanal. | 
| <strong>SequenceNumber</strong> | Die Sequenznummer. Die erste Sequenznummer wird durch Senden eines <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> Befehls angegeben. Jedes Mal, wenn Sie eine andere Abfrage senden, erhöhen Sie diese Zahl um 1. Die Sequenznummer schützt vor Wiedergabeangriffen.    <blockquote>    [!Note]<br />    Es werden zwei separate Sequenznummern verwendet: eine für Befehle und eine für Abfragen.    </blockquote><br /><br /> | 


    

     

2.  Rufen Sie [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)auf.
3.  Der Treiber platziert die Ausgabe der Abfrage in einer [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) Struktur. Auf diese Struktur folgen je nach Abfragetyp zusätzliche Felder.
4.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **omac-Member** der Ausgabestruktur angezeigt wird. Vergleichen Sie dies mit dem Wert des **omac-Elements.** Fehler, wenn sie nicht übereinstimmen.
5.  Vergleichen Sie die Werte der Member **ConfigureType,** **hChannel** und **SequenceNumber** in der Ausgabestruktur mit den Werten für diese Member. Fehler, wenn sie nicht übereinstimmen.
6.  Erhöhen Sie die Sequenznummer für die nächste Abfrage.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 9-Video-APIs](direct3d-video-apis.md)
</dt> </dl>

 

 
