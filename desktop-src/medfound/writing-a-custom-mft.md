---
description: In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Media Foundation Transform (MFT) schreiben.
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Schreiben eines benutzerdefinierten MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c113867c719fc9c8512b5b0e1172ee0694e3905
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471656"
---
# <a name="writing-a-custom-mft"></a>Schreiben eines benutzerdefinierten MFT

In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Media Foundation Transform (MFT) schreiben.

## <a name="mft-checklist"></a>MFT-Prüfliste

Wenn Sie einen benutzerdefinierten MFT implementieren, verwenden Sie die folgende Prüfliste, um die Anforderungen zu bestimmen:




| | | Alle MFTs | Alle MFTs müssen <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>ÜBERTRANSFORM</strong></a>implementieren.<br /> Die folgenden Themen enthalten weitere Informationen zum Implementieren dieser Schnittstelle:<ul><li><a href="basic-mft-processing-model.md">Grundlegendes MFT-Verarbeitungsmodell</a></li><li><a href="time-stamps-and-durations.md">Zeitstempel und Dauer</a></li><li><a href="handling-stream-changes.md">Verarbeiten von Streamänderungen</a></li></ul><br /> | | Encoder und Decoder | Anforderungen: Siehe <a href="implementing-a-codec-mft.md">Implementieren eines Codec-MFT.</a><br /> Empfohlen: Implementieren Sie DIE Benachrichtigungen ZU SERVICE-Qualität (Quality of Service, QoS) , und implementieren Sie <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>DANNQUALQUALITYAdvise</strong></a> oder <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>BENACHRICHTIGUNGENQualityAdvise2.</strong></a><br /> | | Videodecoder und Videoprozessoren | Optional: Unterstützung der DirectX-Videobeschleunigung.<br /><ul><li><a href="direct3d-aware-mfts.md">Direct3D-fähige MFTs</a></li><li><a href="supporting-dxva-2-0-in-media-foundation.md">Unterstützung von DXVA 2.0 in Media Foundation</a></li></ul> | | Hardwarecodecs | Weitere Informationen finden Sie unter <a href="hardware-mfts.md">Hardware-MFTs.</a> | | Damit Ihr MFT von Anwendungen erkannt werden kann, | Weitere Informationen finden Sie unter <a href="registering-and-enumerating-mfts.md">Registrieren und Aufzählen von MFTs.</a> | | Asynchrone datenverarbeitung | Das MFT-Standardmodell verwendet synchrone (blockierende) Aufrufe zum Verarbeiten von Daten. Bei einigen MFTs kann die asynchrone Verarbeitung effizienter sein. Die Implementierung ist jedoch auch komplexer.<br /> Weitere Informationen finden Sie unter <a href="asynchronous-mfts.md">Asynchrone MFTs.</a><br /> | | Ratensteuerung, Trickmodus oder umgekehrte Wiedergabe | Weitere Informationen finden Sie unter <a href="implementing-rate-control.md">Implementieren der Ratensteuerung.</a> | | Wenn Ihr MFT Threads erstellt... | Implementieren Sie die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>SCHNITTSTELLE "REALRealTimeClient".</strong></a> | | Wenn Ihr MFT Über Lizenzierungseinschränkungen verfügt, | Erwägen Sie die Verwendung des Verwendungsfeldmechanismus. Weitere Informationen finden Sie unter <a href="field-of-use-restrictions.md">Field of Use Restrictions (Verwendungseinschränkungen).</a> | | Wenn Sie ein vorhandenes DirectX-Medienobjekt (DMO) portieren, | Siehe <a href="comparison-of-mfts-and-dmos.md">Vergleich von MFTs und DMOs.</a> | 




 

Dieser Abschnitt enthält die folgenden Themen:

-   [Zeitstempel und Dauer](time-stamps-and-durations.md)
-   [Verarbeiten von Streamänderungen](handling-stream-changes.md)
-   [Implementieren eines Codec-MFT](implementing-a-codec-mft.md)
-   [Direct3D-fähige MFTs](direct3d-aware-mfts.md)
-   [Hardware-MFTs](hardware-mfts.md)
-   [Codec-Vererzung](codec-merit.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 




