---
description: In diesem Thema werden Videoinhalte&\# 8211;Schutzfunktionen beschrieben, die ein Grafiktreiber bereitstellen kann.
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: GPU-Based Content Protection mit D3D11 Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24af51187c400c11afa2ea273e7718c2d38ce429
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481736"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a>GPU-Based Content Protection mit D3D11 Video

In diesem Thema werden die Videoinhaltsschutzfunktionen beschrieben, die ein Grafiktreiber bereitstellen kann.

-   [Introduction (Einführung)](#introduction)
-   [Übersicht über den Decodierungsprozess](#overview-of-the-decoding-process)
-   [Verschlüsseln von komprimierten Videopuffern für den Decoder](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. Abfragen der Content Protection Funktionen des Treibers](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Konfigurieren des authentifizierten Kanals](#2-configure-the-authenticated-channel)
    -   [3. Konfigurieren der kryptografischen Sitzung](#3-configure-the-cryptographic-session)
    -   [4. Zuordnen des Decoders zur kryptografischen Sitzung](#4-associate-the-decoder-with-the-cryptographic-session)
-   [Senden von Befehlen für authentifizierte Kanäle](#sending-authenticated-channel-commands)
-   [Senden authentifizierter Kanalabfragen](#sending-authenticated-channel-queries)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das folgende Diagramm zeigt eine vereinfachte Ansicht der Art und Weise, wie geschützte Videoinhalte durch die zu rendernde Pipeline gestreamt werden.

![Ein Diagramm, das geschützte Videoinhalte zeigt.](images/d3d9video01.png)

> [!Note]
>
> Der geschützte Medienpfad (Protected [Media Path,](protected-media-path.md) PMP) ist in diesem Diagramm nicht dargestellt. Der hier gezeigte Datenfluss kann innerhalb eines PMP-Prozesses oder innerhalb eines Anwendungsprozesses auftreten.

 

Der Decoder empfängt verschlüsselte, komprimierte Videodaten von einer externen Quelle. Es wird auch angenommen, dass der Decoder auch einen kryptografischen Schlüssel empfängt, um diese Daten zu entschlüsseln. In diesem Thema wird der Schlüsselaustausch zwischen der Videoquelle und dem Decoder nicht beschrieben, aber der PMP definiert einen möglichen Mechanismus. Die GPU ist in dieser Phase nicht beteiligt.

Für die hardwarebeschleunigte Decodierung übergibt der Softwaredecoder komprimierte Videoinhalte an die GPU. Um diesen Inhalt zu schützen, verschlüsselt der Decoder die Daten erneut, in der Regel mithilfe von AES-CTR, bevor sie an den Hardwarebeschleuniger übergeben werden. Ein Schlüsselaustauschmechanismus wird zwischen dem Decoder und dem Grafiktreiber definiert.

Decodierte Videoframes werden im Videospeicher gespeichert, in der Regel eindeutig. An diesem Punkt werden die Frames verarbeitet und dann dargestellt. Es gibt zwei Hauptoptionen für die Präsentation.

-   Bei Verwendung der D3D9-API können Frames mithilfe einer Hardwareüberlagerung dargestellt werden. Hardware wird in D3D11 nicht unterstützt. Weitere Informationen finden Sie unter [Hardware Overlay Support](hardware-overlay-support.md).
-   Frames können von der Desktopfenster-Verwaltung (Desktop Window Manage, DWM) mithilfe einer freigegebenen Oberfläche dargestellt werden.

Der letzte Schritt besteht im Anzeigen des Frames auf dem Monitor, der möglicherweise Linkschutz zwischen der Grafikkarte und dem Anzeigegerät erfordert. Ein Beispiel für den Linkschutz ist High-Bandwidth Digital Content Protection (HDCP). Der Linkschutz wird mit dem [Ausgabeschutz-Manager](output-protection-manager.md) (Output Protection Manager, OPM) konfiguriert. In diesem Thema wird OPM nicht beschrieben. Weitere Informationen finden Sie unter [Verwenden des Ausgabeschutz-Managers.](using-output-protection-manager.md)

## <a name="overview-of-the-decoding-process"></a>Übersicht über den Decodierungsprozess

Während der hardwarebeschleunigten Decodierung muss der Softwaredecoder komprimierte Videodaten an die Grafikkarte übergeben. Bei Premium-Inhalten müssen diese Daten in der Regel mit symmetrischer Schlüsselverschlüsselung verschlüsselt werden, bevor sie an die GPU gesendet werden.

Um das Video für die Decodierung zu verschlüsseln, verwendet der Softwaredecoder die folgenden Schnittstellen:

-   [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder). Stellt das Decodergerät dar, das auch als Zugriffstaste bezeichnet wird.
-   [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession). Stellt eine kryptografische Sitzung dar, die den Verschlüsselungsschlüssel enthält.
-   [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel). Stellt einen authentifizierten Kanal dar, mit dem der Softwaredecoder die kryptografische Sitzung dem Decoder zuordnen kann.

![Ein Diagramm, das die Direct3d9-Decodierungsschnittstellen zeigt.](images/d3d9video02.png)

Alle diese Schnittstellen werden wie folgt vom Direct3D11-Gerät erhalten:



| Schnittstelle                                                        | Erstellung                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | Rufen [**Sie ID3D11VideoDevice::CreateVideoDecoder auf.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) Der Decodertyp wird durch eine Profil-GUID identifiziert. |
| [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | Rufen [**Sie ID3D11VideoDevice::CreateCryptoSession auf.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession)                                                           |
| [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | Rufen [**Sie ID3D11VideoDevice::CreateAuthenticatedChannel auf.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel)                                             |



 

> [!Note]  
> Um einen Zeiger auf die [**ID3D11VideoDevice-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) zu erhalten, rufen [**Sie QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der [**ID3D11Device-Schnittstelle**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) auf.

 

Der authentifizierte Kanal stellt einen vertrauenswürdigen Kommunikationskanal zwischen dem Softwaredecoder und dem Treiber zur Verfügung. Der Kommunikationskanal funktioniert wie folgt:

-   Der Treiber stellt eine X.509-Zertifikatkette zur Verfügung, deren Stammzertifikat von Microsoft signiert wird.
-   Das Zertifikat enthält einen öffentlichen RSA-Schlüssel für den Treiber.
-   Der Softwaredecoder verwendet den öffentlichen Schlüssel, um dem Treiber einen 128-Bit-AES-Sitzungsschlüssel zu senden.
-   Der Softwaredecoder sendet Abfragen und Befehle an den authentifizierten Kanal.
-   Der Sitzungsschlüssel wird verwendet, um Nachrichtenauthentifizierungscodes (MESSAGE Authentication Codes, MACs) für die Abfragen und Befehle zu berechnen. Der Treiber verwendet die MACs, um die Integrität der Abfrage-/Befehlsdaten zu überprüfen, und der Softwaredecoder verwendet sie, um die Integrität der Antwortdaten des Treibers zu überprüfen.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Verschlüsseln von komprimierten Videopuffern für den Decoder

Im Folgenden finden Sie eine übersicht über den Verschlüsselungs- und Decodierungsprozess:

1.  Der Softwaredecoder empfängt einen Stream verschlüsselter Daten aus der Videoquelle. Der Decoder entschlüsselt diesen Stream.
2.  Der Softwaredecoder handelt einen Sitzungsschlüssel mit der kryptografischen Sitzung aus.
3.  Der Softwaredecoder verwendet den authentifizierten Kanal, um die kryptografische Sitzung dem Decodergerät zu zuordnen.
4.  Der Softwaredecoder legt komprimierte Daten in Puffern ab, die vom Decodergerät (Accelerator) empfangen werden. Bei geschützten Inhalten verschlüsselt der Softwareencoder die Daten, die in den Puffern gespeichert werden, mithilfe des Sitzungsschlüssels für die Verschlüsselung.
    > [!Note]  
    > Einige Treiber verwenden anstelle des Sitzungsschlüssels einen Inhaltsschlüssel für die Verschlüsselung. Der Inhaltsschlüssel kann sich von einem Frame zum nächsten ändern.

     

5.  Der Decoder übermittelt die verschlüsselten komprimierten Puffer an die Zugriffstaste. Bei AES-CTR übergibt der Decoder auch den Initialisierungsvektor. Wenn ein Inhaltsschlüssel verwendet wird, übergibt der Decoder den Inhaltsschlüssel, der mit dem Sitzungsschlüssel verschlüsselt wurde.

Direct3D11 verfügt über Standardunterstützung für 128-Bit-AES-CTR, ist aber für die Erweiterung auf zusätzliche Verschlüsselungstypen konzipiert.

In den nächsten fünf Abschnitten finden Sie ausführlichere Schritte.

-   [1. Abfragen der Content Protection Funktionen des Treibers](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Konfigurieren des authentifizierten Kanals](#2-configure-the-authenticated-channel)
-   [3. Konfigurieren der kryptografischen Sitzung](#3-configure-the-cryptographic-session)
-   [4. Zuordnen des Decoders zur kryptografischen Sitzung](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. Abfragen der Content Protection Funktionen des Treibers

Bevor Sie versuchen, die Verschlüsselung anzuwenden, erhalten Sie die Inhaltsschutzfunktionen des Treibers.

1.  Sie erhalten einen Zeiger auf die ID3D11Device-Schnittstelle.
2.  Rufen [**Sie QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die [**SCHNITTSTELLE ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) auf.
3.  Rufen [**Sie ID3D11VideoDevice::GetContentProtectionCaps auf.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps) Diese Methode füllt eine [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) mit den Inhaltsschutzfunktionen des Treibers aus.

Suchen Sie insbesondere nach den folgenden Funktionen:

-   Wenn das **Caps-Member** **das** D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE **oder** D3D11_CONTENT_PROTECTION_CAPS_HARDWARE enthält, kann der Treiber die Verschlüsselung durchführen.
-   Wenn das **Caps-Member** das **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** enthält, verwendet der Treiber einen separaten Inhaltsschlüssel für die Entschlüsselung.
-   Rufen [**Sie ID3D11VideoDevice::CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) auf, um zu bestimmen, welche Arten von Schlüsselaustausch der Treiber zum Generieren des Sitzungsschlüssels unterstützt.

Zusätzliche Funktionen werden im **Caps-Member** angegeben.

### <a name="2-configure-the-authenticated-channel"></a>2. Konfigurieren des authentifizierten Kanals

Der nächste Schritt besteht im Konfigurieren des authentifizierten Kanals.

1.  Rufen [**Sie ID3D11VideoDevice::CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) auf, um den authentifizierten Kanal zu erstellen. Geben Sie für den *ChannelType-Parameter* einen Kanaltyp an, der den Funktionen des Treibers entspricht.
    -   Der **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** Kanaltyp entspricht **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.
    -   Der **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** Kanaltyp entspricht **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.

    Die **CreateAuthenticatedChannel-Methode** gibt einen Zeiger auf die [**ID3D11AuthenticatedChannel-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) zurück.
2.  Rufen Sie [**ID3D11AuthenticatedChannel::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) auf, um die Größe des X.509-Zertifikats des Treibers abzurufen. Ordnen Sie einen Puffer der erforderlichen Größe zu.
3.  Rufen Sie [**ID3D11AuthenticatedChannel::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) auf, um das Zertifikat abzurufen. Die -Methode kopiert das Zertifikat in den Puffer, der im vorherigen Schritt zugeordnet wurde.
4.  Vergewissern Sie sich, dass das Zertifikat des Treibers von Microsoft signiert und nicht widerrufen wurde.
5.  Abrufen des öffentlichen Schlüssels aus dem Zertifikat.
6.  Generieren Sie einen zufälligen RSA-Sitzungsschlüssel. Dieser Sitzungsschlüssel wird zum Signieren von Daten verwendet, die an den authentifizierten Kanal gesendet werden. Verschlüsseln Sie den Sitzungsschlüssel mit dem öffentlichen Schlüssel des Treibers.
7.  Rufen Sie [**ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) auf, um den verschlüsselten Sitzungsschlüssel an den Treiber zu senden.
8.  Initialisieren Sie den sicheren Kanal wie folgt:
    1.  Füllen Sie eine [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) Struktur aus, wie in der Dokumentation beschrieben.
    2.  Senden Sie den [**befehl D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT,**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) indem Sie [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) aufrufen, wie im Abschnitt [Senden von Befehlen](#sending-authenticated-channel-commands)für authentifizierte Kanäle beschrieben. Dieser Befehl enthält die Anfangssequenznummern für die Befehle und Abfragen, die an den authentifizierten Kanal gesendet werden.
9.  Überprüfen Sie den Kanaltyp, indem Sie eine [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) Abfrage an den authentifizierten Kanal senden, wie im Abschnitt Senden von Abfragen für [authentifizierte Kanäle](#sending-authenticated-channel-queries)beschrieben. Überprüfen Sie, ob der Kanaltyp mit dem übereinstimmt, den Sie in der [**CreateAuthenticatedChannel-Methode**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) angegeben haben.

### <a name="3-configure-the-cryptographic-session"></a>3. Konfigurieren der Kryptografiesitzung

Konfigurieren Sie als Nächstes die kryptografische Sitzung, und richten Sie den Sitzungsschlüssel ein.

1.  Rufen Sie [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) auf, um die kryptografische Sitzung zu erstellen. Diese Methode gibt einen Zeiger auf die [**ID3D11CryptoSession-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) zurück.
2.  Rufen Sie [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) auf, um die Größe des X.509-Zertifikats des Treibers abzurufen. Ordnen Sie einen Puffer der erforderlichen Größe zu.
3.  Rufen Sie [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) auf, um das Zertifikat abzurufen. Die -Methode kopiert das Zertifikat in den Puffer, der im vorherigen Schritt zugeordnet wurde.
4.  Vergewissern Sie sich, dass das Zertifikat des Treibers von Microsoft signiert und nicht widerrufen wurde.
5.  Abrufen des öffentlichen Schlüssels aus dem Zertifikat.
6.  Generieren Sie einen zufälligen RSA-Sitzungsschlüssel. Dies ist ein separater Sitzungsschlüssel vom Sitzungsschlüssel des authentifizierten Kanals. Verschlüsseln Sie den Sitzungsschlüssel mit dem öffentlichen Schlüssel des Treibers.
7.  Rufen Sie [**ID3D11VideoContext::NegotiateCryptoSessionKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) auf, um den verschlüsselten Sitzungsschlüssel an den Treiber zu senden.
8.  Wenn die Inhaltsschutzfunktionen **3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** enthalten, erstellen Sie einen zufälligen RSA-Inhaltsschlüssel. Dies wird später im Decodierungsprozess verwendet.

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a>4. Zuordnen des Decoders zur Kryptografiesitzung

Ordnen Sie als Nächstes das Decodergerät wie folgt dem Direct3D11-Gerät und der kryptografischen Sitzung zu:

1.  Erhalten Sie ein Handle für das Direct3D11-Gerät, indem Sie eine [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) Abfrage an den authentifizierten Kanal senden.
2.  Füllen Sie eine [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT-Struktur**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) mit den folgenden Informationen aus:
    -   Legen Sie den **DecodeHandle-Member** auf das handle fest, das von [**ID3D11VideoDecoder::GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle)zurückgegeben wird.
    -   Legen Sie den **CryptoSessionHandle-Member** auf das handle fest, das von [**ID3D11CryptoSession::GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle)zurückgegeben wird.
    -   Legen Sie das **DeviceHandle-Element** auf das Direct3D11-Gerätehandle fest.
3.  Rufen Sie [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) auf, um einen [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) Befehl an den authentifizierten Kanal zu senden.

Das folgende Diagramm veranschaulicht den Austausch von Handles:

![Ein Diagramm, das zeigt, wie der Dxva-Decoder der kryptografischen Sitzung zugeordnet ist.](images/d3d9video03.png)

Der Softwaredecoder kann jetzt den kryptografischen Sitzungsschlüssel verwenden, um die komprimierten Videopuffer zu verschlüsseln. Jeder komprimierte Puffer verfügt über einen eigenen Initialisierungsvektor (IV), der im **pIV-Member** der [**D3D11_VIDEO_DECODER_BUFFER_DESC-Struktur**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) angegeben ist.

## <a name="sending-authenticated-channel-commands"></a>Senden von Befehlen für authentifizierte Kanäle

Eine Reihe von Befehlen wird zum Konfigurieren des authentifizierten Kanals und zum Festlegen verschiedener Inhaltsschutzfunktionen definiert. Eine Liste der Befehle finden Sie unter [Content Protection Befehle.](content-protection-commands.md)

Führen Sie die folgenden Schritte aus, um einen Befehl an den authentifizierten Kanal zu senden.

1.  Füllen Sie die Eingabedatenstruktur aus. Diese Datenstruktur ist immer eine [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) Struktur gefolgt von zusätzlichen Feldern. Füllen Sie die **D3D11_AUTHENTICATED_CONFIGURE_INPUT** Struktur aus, wie in der folgenden Tabelle dargestellt.

    
| Member | BESCHREIBUNG | 
|--------|-------------|
| <strong>omac</strong> | Überspringen Sie dieses Feld vorerst. | 
| <strong>ConfigureType</strong> | GUID, die den Befehl identifiziert. Eine Liste der Befehle finden Sie unter <a href="content-protection-commands.md">Content Protection Befehle.</a> | 
| <strong>hChannel</strong> | Das Handle für den authentifizierten Kanal. | 
| <strong>SequenceNumber</strong> | Die Sequenznummer. Die erste Sequenznummer wird durch Senden eines <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> Befehls angegeben. Jedes Mal, wenn Sie einen anderen Befehl senden, erhöhen Sie diese Zahl um 1. Die Sequenznummer schützt vor Wiedergabeangriffen.    <blockquote>    [!Note]<br />    Es werden zwei separate Sequenznummern verwendet: eine für Befehle und eine für Abfragen.    </blockquote><br /><br /> | 


    

     

2.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **omac-Element** der Eingabestruktur angezeigt wird. Kopieren Sie dann diesen Tagwert in das **omac-Element.**
3.  Rufen Sie [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel)auf.
4.  Der Treiber platziert die Ausgabe des Befehls in der [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) Struktur.
5.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **omac-Member** der Ausgabestruktur angezeigt wird. Vergleichen Sie dies mit dem Wert des **omac-Elements.** Fehler, wenn sie nicht übereinstimmen.
6.  Vergleichen Sie die Werte der Member **ConfigureType,** **hChannel** und **SequenceNumber** in der Ausgabestruktur mit den Werten für diese Member. Fehler, wenn sie nicht übereinstimmen.
7.  Erhöhen Sie die Sequenznummer für den nächsten Befehl.

## <a name="sending-authenticated-channel-queries"></a>Senden authentifizierter Kanalabfragen

Für das Abrufen von Informationen über den authentifizierten Kanal wird eine Reihe von Abfragen definiert. Eine Liste der Abfragen finden Sie unter [Content Protection Abfragen.](content-protection-queries.md)

Führen Sie die folgenden Schritte aus, um einen Befehl an den authentifizierten Kanal zu senden.

1.  Füllen Sie die Eingabedatenstruktur aus. Diese Datenstruktur ist immer eine [**D3D11_AUTHENTICATED_QUERY_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) Struktur, möglicherweise gefolgt von zusätzlichen Feldern. Füllen Sie die **D3D11_AUTHENTICATED_QUERY_INPUT** Struktur aus, wie in der folgenden Tabelle dargestellt.

    
| Member | BESCHREIBUNG | 
|--------|-------------|
| <strong>QueryType</strong> | GUID, die die Abfrage identifiziert. Eine Liste der Abfragen finden Sie unter <a href="content-protection-queries.md">Content Protection Abfragen.</a> | 
| <strong>hChannel</strong> | Das Handle für den authentifizierten Kanal. | 
| <strong>SequenceNumber</strong> | Die Sequenznummer. Die erste Sequenznummer wird durch Senden eines <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> Befehls angegeben. Jedes Mal, wenn Sie eine andere Abfrage senden, erhöhen Sie diese Zahl um 1. Die Sequenznummer schützt vor Wiedergabeangriffen.    <blockquote>    [!Note]<br />    Es werden zwei separate Sequenznummern verwendet: eine für Befehle und eine für Abfragen.    </blockquote><br /><br /> | 


    

     

2.  Rufen Sie [**ID3D11VideoContext::QueryAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel)auf.
3.  Der Treiber platziert die Ausgabe der Abfrage in einer [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) Struktur. Auf diese Struktur folgen je nach Abfragetyp zusätzliche Felder.
4.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **omac-Member** der Ausgabestruktur angezeigt wird. Vergleichen Sie dies mit dem Wert des **omac-Elements.** Fehler, wenn sie nicht übereinstimmen.
5.  Vergleichen Sie die Werte der Member **ConfigureType,** **hChannel** und **SequenceNumber** in der Ausgabestruktur mit den Werten für diese Member. Fehler, wenn sie nicht übereinstimmen.
6.  Erhöhen Sie die Sequenznummer für die nächste Abfrage.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 Video-APIs](direct3d-11-video-apis.md)
</dt> </dl>

 

 
