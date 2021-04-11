---
description: In diesem Thema werden Videoinhalte&\# 8211 und Schutzfunktionen beschrieben, die von einem Grafiktreiber bereitgestellt werden können.
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: GPU-Based Content Protection mit D3D11-Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78097492d375d50688f2472f5d2de99cc21f8594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041546"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a>GPU-Based Content Protection mit D3D11-Video

In diesem Thema werden Videoinhalte – Schutzfunktionen beschrieben, die von einem Grafiktreiber bereitgestellt werden können.

-   [Introduction (Einführung)](#introduction)
-   [Übersicht über den Decodierungs Prozess](#overview-of-the-decoding-process)
-   [Verschlüsseln komprimierter Video Puffer für den Decoder](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. Abfragen der Content Protection Funktionen des Treibers](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Konfigurieren des authentifizierten Kanals](#2-configure-the-authenticated-channel)
    -   [3. Konfigurieren der Kryptografiesitzung](#3-configure-the-cryptographic-session)
    -   [4. Ordnen Sie den Decoder der Kryptografiesitzung zu.](#4-associate-the-decoder-with-the-cryptographic-session)
-   [Senden von authentifizierten Kanal Befehlen](#sending-authenticated-channel-commands)
-   [Senden von authentifizierten Kanal Abfragen](#sending-authenticated-channel-queries)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das folgende Diagramm zeigt eine vereinfachte Ansicht, wie Inhalte geschützter Videos durch die Pipeline durchlaufen werden, die gerendert werden soll.

![ein Diagramm, in dem geschützte Videoinhalte angezeigt werden.](images/d3d9video01.png)

> [!Note]
>
> Der [geschützte Medien Pfad](protected-media-path.md) (PMP) ist in diesem Diagramm nicht dargestellt. Der hier gezeigte Datenfluss kann in einem PMP-Prozess oder innerhalb eines Anwendungsprozesses auftreten.

 

Der Decoder empfängt verschlüsselte, komprimierte Videodaten aus einer externen Quelle. Außerdem wird davon ausgegangen, dass der Decoder auch einen kryptografischen Schlüssel erhält, um diese Daten zu entschlüsseln. In diesem Thema wird nicht der Schlüsselaustausch zwischen der Videoquelle und dem Decoder beschrieben, aber das PMP definiert einen möglichen Mechanismus. Die GPU ist an dieser Phase nicht beteiligt.

Bei der Hardware beschleunigten Decodierung übergibt der Software Decoder komprimierte Videoinhalte an die GPU. Um diesen Inhalt zu schützen, verschlüsselt der Decoder die Daten, in der Regel AES-CTR, erneut, bevor Sie an den Hardwarebeschleuniger übergeben werden. Zwischen dem Decoder und dem Grafiktreiber wird ein Schlüsselaustausch Mechanismus definiert.

Decodierte Video Frames werden im Videospeicher gespeichert, in der Regel im Klartext. An diesem Punkt werden die Frames verarbeitet und dann dargestellt. Es gibt zwei Hauptoptionen für die Präsentation.

-   Wenn Sie die d3d9-API verwenden, können Frames mithilfe eines Hardware Überlagerungs Fensters angezeigt werden. Hardware übermäßig wird in D3D11 nicht unterstützt. Weitere Informationen finden Sie [unter Unterstützung für Hardware Überlagerung](hardware-overlay-support.md).
-   Frames können von der Desktop Fensterverwaltung (DWM) mithilfe einer freigegebenen Oberfläche dargestellt werden.

Der letzte Schritt besteht darin, den Frame auf dem Monitor anzuzeigen, der möglicherweise einen Link Schutz zwischen der Grafikkarte und dem Anzeigegerät erfordert. Ein Beispiel für den Link Schutz ist High-Bandwidth Digital Content Protection (HDCP). Der Link Schutz wird mithilfe von [Output Protection Manager](output-protection-manager.md) (OPM) konfiguriert. OPM wird in diesem Thema nicht beschrieben. Weitere Informationen finden Sie unter [Verwenden von Output Protection Manager](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Übersicht über den Decodierungs Prozess

Während der Hardware beschleunigten Decodierung muss der Software Decoder komprimierte Videodaten an die Grafikkarte übergeben. Bei Premium-Inhalten müssen diese Daten in der Regel mithilfe der Verschlüsselung mit symmetrischen Schlüsseln verschlüsselt werden, bevor Sie an die GPU gesendet werden.

Zum Verschlüsseln des Videos für die Decodierung verwendet der Software Decoder die folgenden Schnittstellen:

-   [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder). Stellt das Decoder-Gerät dar, das auch als Accelerator bezeichnet wird.
-   [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession). Stellt eine Kryptografiesitzung dar, die den Verschlüsselungsschlüssel bereitstellt.
-   [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel). Stellt einen authentifizierten Kanal dar, der es dem Software Decoder ermöglicht, die Kryptografiesitzung dem Decoder zuzuordnen.

![ein Diagramm, das die von Direct3D9-Decodierungs Schnittstellen anzeigt.](images/d3d9video02.png)

Alle diese Schnittstellen werden vom Direct3D11-Gerät wie folgt abgerufen:



| Schnittstelle                                                        | Erstellung                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | Aufrufen von [**ID3D11VideoDevice:: createvideodecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview). Der Decodertyp wird durch eine Profil-GUID identifiziert. |
| [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | Aufrufen von [**ID3D11VideoDevice:: anatecrypdesession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession).                                                           |
| [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | Aufrufen von [**ID3D11VideoDevice:: kreateauthentiinitiedchannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel).                                             |



 

> [!Note]  
> Um einen Zeiger auf die [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) -Schnittstelle abzurufen, nennen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in der [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) -Schnittstelle.

 

Der authentifizierte Kanal bietet einen vertrauenswürdigen Kommunikationskanal zwischen dem Software Decoder und dem Treiber. Der Kommunikationskanal funktioniert wie folgt:

-   Der Treiber stellt eine X. 509-Zertifikat Kette bereit, deren Stamm Zertifikat von Microsoft signiert ist.
-   Das Zertifikat enthält einen öffentlichen RSA-Schlüssel für den Treiber.
-   Der Software Decoder verwendet den öffentlichen Schlüssel, um dem Treiber einen 128-Bit-AES-Sitzungsschlüssel zu senden.
-   Der Software Decoder sendet Abfragen und Befehle an den authentifizierten Kanal.
-   Der Sitzungsschlüssel wird zum Berechnen von Nachrichten Authentifizierungscodes (Macs) für die Abfragen und Befehle verwendet. Der Treiber verwendet die Macs, um die Integrität der Abfrage-/Befehlsdaten zu überprüfen, und der Software Decoder verwendet diese, um die Integrität der Antwortdaten des Treibers zu überprüfen.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Verschlüsseln komprimierter Video Puffer für den Decoder

Im folgenden finden Sie eine allgemeine Übersicht über den Verschlüsselungs-und Decodierungs Prozess:

1.  Der Software Decoder empfängt einen Stream verschlüsselter Daten aus der Videoquelle. Der Decoder entschlüsselt diesen Datenstrom.
2.  Der Software Decoder aushandiert einen Sitzungsschlüssel mit der Kryptografiesitzung.
3.  Der Software Decoder verwendet den authentifizierten Kanal, um die Kryptografiesitzung dem Decoder-Gerät zuzuordnen.
4.  Der Software Decoder fügt komprimierte Daten in Puffer ein, die vom Decoder-Gerät (Accelerator) abgerufen werden. Für geschützte Inhalte verschlüsselt der Software Encoder die Daten, die in die Puffer eingefügt werden, unter Verwendung des Sitzungsschlüssels für die Verschlüsselung.
    > [!Note]  
    > Einige Treiber verwenden einen Inhalts Schlüssel anstelle des Sitzungsschlüssels für die Verschlüsselung. Der Inhalts Schlüssel kann sich von einem Frame zur nächsten ändern.

     

5.  Der Decoder übergibt die verschlüsselten komprimierten Puffer an die Zugriffstaste. Für AES-CTR übergibt der Decoder auch den Initialisierungs Vektor. Wenn ein Inhalts Schlüssel verwendet wird, übergibt der Decoder den Inhalts Schlüssel, der mit dem Sitzungsschlüssel verschlüsselt wurde.

Direct3D11 verfügt über Standardunterstützung für 128-Bit-AES-CTR, wurde jedoch für die Erweiterung auf zusätzliche Verschlüsselungstypen entwickelt.

In den nächsten fünf Abschnitten finden Sie ausführlichere Schritte.

-   [1. Abfragen der Content Protection Funktionen des Treibers](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Konfigurieren des authentifizierten Kanals](#2-configure-the-authenticated-channel)
-   [3. Konfigurieren der Kryptografiesitzung](#3-configure-the-cryptographic-session)
-   [4. Ordnen Sie den Decoder der Kryptografiesitzung zu.](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. Abfragen der Content Protection Funktionen des Treibers

Bevor Sie versuchen, die Verschlüsselung anzuwenden, sollten Sie die inhaltsschutzfunktionen des Treibers erhalten.

1.  Einen Zeiger auf die ID3D11Device-Schnittstelle erhalten.
2.  Ruft [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) -Schnittstelle auf.
3.  Aufrufen von [**ID3D11VideoDevice:: getcontentschutzcaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps). Diese Methode füllt eine [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) Struktur mit den inhaltsschutzfunktionen des Treibers aus.

Achten Sie insbesondere auf die folgenden Funktionen:

-   Wenn das **Caps** -Mitglied die **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE** oder **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE** -Flag enthält, kann der Treiber die Verschlüsselung ausführen.
-   Wenn das **Caps** -Element das **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** -Flag enthält, verwendet der Treiber einen separaten Inhalts Schlüssel für die Entschlüsselung.
-   Rufen Sie [**ID3D11VideoDevice:: checkcryptokeyexchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) auf, um zu bestimmen, welche Typen von Schlüsselaustausch der Treiber zum Erstellen des Sitzungsschlüssels unterstützt.

Zusätzliche Funktionen werden im **Caps** -Member angezeigt.

### <a name="2-configure-the-authenticated-channel"></a>2. Konfigurieren des authentifizierten Kanals

Der nächste Schritt besteht darin, den authentifizierten Kanal zu konfigurieren.

1.  Rufen Sie [**ID3D11VideoDevice:: kreateauthentiinitiedchannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) auf, um den authentifizierten Kanal zu erstellen. Geben Sie für den *channelType* -Parameter einen Kanaltyp an, der mit den Funktionen des Treibers übereinstimmt.
    -   Der **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** Kanaltyp entspricht **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.
    -   Der **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** Kanaltyp entspricht **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.

    Die Methode " **kreateauthentiinitiedchannel** " gibt einen Zeiger auf die [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) -Schnittstelle zurück.
2.  Aufrufen von [**ID3D11AuthenticatedChannel:: getcertifikatesize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) zum Abrufen der Größe des X. 509-Zertifikats des Treibers. Weisen Sie einen Puffer mit der erforderlichen Größe zu.
3.  Aufrufen von [**ID3D11AuthenticatedChannel:: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) zum Abrufen des Zertifikats. Die-Methode kopiert das Zertifikat in den Puffer, der im vorherigen Schritt zugeordnet wurde.
4.  Vergewissern Sie sich, dass das Zertifikat des Treibers von Microsoft signiert wurde und nicht widerrufen wurde.
5.  Den öffentlichen Schlüssel aus dem Zertifikat zu erhalten.
6.  Generieren Sie einen zufälligen RSA-Sitzungsschlüssel. Dieser Sitzungsschlüssel wird zum Signieren von Daten verwendet, die an den authentifizierten Kanal gesendet werden. Verschlüsseln Sie den Sitzungsschlüssel mit dem öffentlichen Schlüssel des Treibers.
7.  Aufrufen von [**ID3D11VideoContext:: aushandateauthentitoredchannelkeyexchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) , um den verschlüsselten Sitzungsschlüssel an den Treiber zu senden.
8.  Initialisieren Sie den sicheren Kanal wie folgt:
    1.  Füllen Sie eine [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) Struktur aus, wie in der Dokumentation beschrieben.
    2.  Senden Sie den [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) Befehl, indem Sie [**ID3D11VideoContext:: Konfigurations reauthentiinitiedchannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) aufrufen, wie im Abschnitt [Senden von authentifizierten Kanal Befehlen](#sending-authenticated-channel-commands)beschrieben. Dieser Befehl enthält die Startsequenz Nummern für die Befehle und Abfragen, die an den authentifizierten Kanal gesendet werden.
9.  Überprüfen Sie den Kanaltyp, indem Sie eine [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) Abfrage an den authentifizierten Kanal senden, wie im Abschnitt [Senden von authentifizierten Kanal Abfragen](#sending-authenticated-channel-queries)beschrieben. Überprüfen Sie, ob der Kanaltyp mit dem übereinstimmt [**, den Sie in der Methode "**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) Methode" von "" aufgerufen haben.

### <a name="3-configure-the-cryptographic-session"></a>3. Konfigurieren der Kryptografiesitzung

Konfigurieren Sie als nächstes die Kryptografiesitzung, und legen Sie den Sitzungsschlüssel fest.

1.  Rufen Sie [**ID3D11VideoDevice:: featecrypdesession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) auf, um die Kryptografiesitzung zu erstellen. Diese Methode gibt einen Zeiger auf die [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) -Schnittstelle zurück.
2.  Aufrufen von [**ID3D11CryptoSession:: getcertifikatesize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) zum Abrufen der Größe des X. 509-Zertifikats des Treibers. Weisen Sie einen Puffer mit der erforderlichen Größe zu.
3.  Aufrufen von [**ID3D11CryptoSession:: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) zum Abrufen des Zertifikats. Die-Methode kopiert das Zertifikat in den Puffer, der im vorherigen Schritt zugeordnet wurde.
4.  Vergewissern Sie sich, dass das Zertifikat des Treibers von Microsoft signiert wurde und nicht widerrufen wurde.
5.  Den öffentlichen Schlüssel aus dem Zertifikat zu erhalten.
6.  Generieren Sie einen zufälligen RSA-Sitzungsschlüssel. Dabei handelt es sich um einen separaten Sitzungsschlüssel aus dem authentifizierten channelsitzungsschlüssel. Verschlüsseln Sie den Sitzungsschlüssel mit dem öffentlichen Schlüssel des Treibers.
7.  Wenden Sie [**ID3D11VideoContext:: aushandatecryptosessionkeyexchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) an, um den verschlüsselten Sitzungsschlüssel an den Treiber zu senden.
8.  Wenn die inhaltsschutzfunktionen **3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** enthalten, erstellen Sie einen zufälligen RSA-Inhalts Schlüssel. Diese wird später im Decodierungs Vorgang verwendet.

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a>4. Ordnen Sie den Decoder der Kryptografiesitzung zu.

Ordnen Sie anschließend das Decoder-Gerät wie folgt dem Direct3D11-Gerät und der Kryptografiesitzung zu:

1.  Sie erhalten ein Handle für das Direct3D11-Gerät, indem Sie eine [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) Abfrage an den authentifizierten Kanal senden.
2.  Fügen Sie eine [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) Struktur mit den folgenden Informationen ein:
    -   Legen Sie den **decodehandle** -Member auf das von [**ID3D11VideoDecoder:: getdriverhandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle)zurückgegebene Handle fest.
    -   Legen Sie den **cryptosessionhandle** -Member auf das von [**ID3D11CryptoSession:: getcryptosessionhandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle)zurückgegebene Handle fest.
    -   Legen Sie das Element " **envicehandle** " auf das Direct3D11-Geräte Handle fest.
3.  Wenden Sie [**ID3D11VideoContext:: konfigurierten reauthentiinitiedchannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) an, um einen [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) Befehl an den authentifizierten Kanal zu senden.

Das folgende Diagramm veranschaulicht den Austausch von Handles:

![ein Diagramm, das zeigt, wie der DXVA-Decoder der Kryptografiesitzung zugeordnet wird.](images/d3d9video03.png)

Der Software Decoder kann nun den kryptografiesitzungsschlüssel verwenden, um die komprimierten Video Puffer zu verschlüsseln. Jeder komprimierte Puffer verfügt über einen eigenen Initialisierungs Vektor (IV), der im **PIV** -Member der [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) Struktur angegeben wird.

## <a name="sending-authenticated-channel-commands"></a>Senden von authentifizierten Kanal Befehlen

Ein Satz von Befehlen wird zum Konfigurieren des authentifizierten Kanals und zum Festlegen verschiedener Inhalts Schutzmaßnahmen definiert. Eine Liste der Befehle finden Sie unter [Content Protection-Befehle](content-protection-commands.md).

Führen Sie die folgenden Schritte aus, um einen Befehl an den authentifizierten Kanal zu senden.

1.  Füllen Sie die Eingabedaten Struktur aus. Diese Datenstruktur ist immer eine [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) Struktur, gefolgt von zusätzlichen Feldern. Füllen Sie die **D3D11_AUTHENTICATED_CONFIGURE_INPUT** Struktur aus, wie in der folgenden Tabelle gezeigt.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Member</th>
    <th>BESCHREIBUNG</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>OMAC</strong></td>
    <td>Dieses Feld jetzt überspringen.</td>
    </tr>
    <tr class="even">
    <td><strong>Konfiguriertyp</strong></td>
    <td>GUID, die den Befehl identifiziert. Eine Liste der Befehle finden Sie unter <a href="content-protection-commands.md">Content Protection-Befehle</a>.</td>
    </tr>
    <tr class="odd">
    <td><strong>hchannel</strong></td>
    <td>Das Handle für den authentifizierten Kanal.</td>
    </tr>
    <tr class="even">
    <td><strong>SequenceNumber</strong></td>
    <td>Die Sequenznummer. Die erste Sequenznummer wird durch Senden eines <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> Befehls angegeben. Jedes Mal, wenn Sie einen anderen Befehl senden, erhöhen Sie diese Zahl um 1. Die Sequenznummer schützt vor Replay-Angriffen.
    <blockquote>
    [!Note]<br />
Es werden zwei separate Sequenznummern verwendet, eine für Befehle und eine für Abfragen.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **OMAC** -Member der Eingabe Struktur angezeigt wird. Kopieren Sie dann diesen Tagwert in den **OMAC** -Member.
3.  Ruft [**ID3D11VideoContext:: konfigurierten reauthentiinitiedchannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel)auf.
4.  Der Treiber legt die Ausgabe aus dem Befehl in der [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) Struktur ab.
5.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **OMAC** -Member der Ausgabestruktur angezeigt wird. Vergleichen Sie dies mit dem Wert des **OMAC** -Members. Schlägt fehl, wenn Sie nicht stimmen.
6.  Vergleichen Sie die Werte der Member " **konfiguritytype**", " **hchannel**" und " **SequenceNumber** " in der Ausgabestruktur mit ihren Werten für diese Elemente. Schlägt fehl, wenn Sie nicht stimmen.
7.  Erhöhen Sie die Sequenznummer für den nächsten Befehl.

## <a name="sending-authenticated-channel-queries"></a>Senden von authentifizierten Kanal Abfragen

Ein Satz von Abfragen wird zum Abrufen von Informationen über den authentifizierten Kanal definiert. Eine Liste der Abfragen finden Sie unter [Content Protection-Abfragen](content-protection-queries.md).

Führen Sie die folgenden Schritte aus, um einen Befehl an den authentifizierten Kanal zu senden.

1.  Füllen Sie die Eingabedaten Struktur aus. Diese Datenstruktur ist immer eine [**D3D11_AUTHENTICATED_QUERY_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) Struktur, der möglicherweise zusätzliche Felder folgt. Füllen Sie die **D3D11_AUTHENTICATED_QUERY_INPUT** Struktur aus, wie in der folgenden Tabelle gezeigt.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Member</th>
    <th>BESCHREIBUNG</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>QueryType</strong></td>
    <td>GUID, die die Abfrage identifiziert. Eine Liste der Abfragen finden Sie unter <a href="content-protection-queries.md">Content Protection-Abfragen</a>.</td>
    </tr>
    <tr class="even">
    <td><strong>hchannel</strong></td>
    <td>Das Handle für den authentifizierten Kanal.</td>
    </tr>
    <tr class="odd">
    <td><strong>SequenceNumber</strong></td>
    <td>Die Sequenznummer. Die erste Sequenznummer wird durch Senden eines <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> Befehls angegeben. Jedes Mal, wenn Sie eine andere Abfrage senden, erhöhen Sie diese Zahl um 1. Die Sequenznummer schützt vor Replay-Angriffen.
    <blockquote>
    [!Note]<br />
Es werden zwei separate Sequenznummern verwendet, eine für Befehle und eine für Abfragen.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  [**ID3D11VideoContext:: queryauthentiinitiedchannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel)aufzurufen.
3.  Der Treiber legt die Ausgabe der Abfrage in einer [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) Struktur ab. Auf diese Struktur folgen je nach Abfragetyp zusätzliche Felder.
4.  Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **OMAC** -Member der Ausgabestruktur angezeigt wird. Vergleichen Sie dies mit dem Wert des **OMAC** -Members. Schlägt fehl, wenn Sie nicht stimmen.
5.  Vergleichen Sie die Werte der Member " **konfiguritytype**", " **hchannel**" und " **SequenceNumber** " in der Ausgabestruktur mit ihren Werten für diese Elemente. Schlägt fehl, wenn Sie nicht stimmen.
6.  Erhöhen Sie die Sequenznummer für die nächste Abfrage.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11-Video-APIs](direct3d-11-video-apis.md)
</dt> </dl>

 

 
