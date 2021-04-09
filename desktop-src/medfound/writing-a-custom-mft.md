---
description: In diesem Abschnitt wird beschrieben, wie eine benutzerdefinierte Media Foundation Transformation (MFT) geschrieben wird.
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Schreiben eines benutzerdefinierten MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865571"
---
# <a name="writing-a-custom-mft"></a>Schreiben eines benutzerdefinierten MFT

In diesem Abschnitt wird beschrieben, wie eine benutzerdefinierte Media Foundation Transformation (MFT) geschrieben wird.

## <a name="mft-checklist"></a>MFT-Checkliste

Wenn Sie einen benutzerdefinierten MFT implementieren, verwenden Sie die folgende Checkliste, um die Anforderungen zu bestimmen:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Alle MFTs</td>
<td>Alle MFTs müssen " <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMF Transform</strong></a>" implementieren.<br/> Die folgenden Themen stellen weitere Informationen zur Implementierung dieser Schnittstelle zur Verfügung:
<ul>
<li><a href="basic-mft-processing-model.md">Einfaches MFT-Verarbeitungsmodell</a></li>
<li><a href="time-stamps-and-durations.md">Zeitstempel und Dauer</a></li>
<li><a href="handling-stream-changes.md">Verarbeiten von streamänderungen</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Encoder und Decoder</td>
<td>Anforderungen: siehe <a href="implementing-a-codec-mft.md">Implementieren eines Codec-MFT</a>.<br/> Empfohlen: Implementieren Sie <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>imfqualityrecommended</strong></a> oder <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, um QoS-Benachrichtigungen (Quality of Service) zu unterstützen.<br/></td>
</tr>
<tr class="odd">
<td>Video-Decoder und Video Prozessoren</td>
<td>Optional: Unterstützung der DirectX-Video Beschleunigung.<br/>
<ul>
<li><a href="direct3d-aware-mfts.md">Direct3D-kompatible MFTs</a></li>
<li><a href="supporting-dxva-2-0-in-media-foundation.md">Unterstützung von DXVA 2,0 in Media Foundation</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Hardware-Codecs</td>
<td>Siehe <a href="hardware-mfts.md">Hardware-MFTs</a>.</td>
</tr>
<tr class="odd">
<td>So machen Sie die MFT durch Anwendungen auffindbar...</td>
<td>Weitere Informationen finden Sie unter <a href="registering-and-enumerating-mfts.md">registrieren und Auflisten von MFTs</a>.</td>
</tr>
<tr class="even">
<td>Asynchrone Datenverarbeitung</td>
<td>Das MFT-Standardmodell verwendet synchrone (blockierende) Aufrufe, um Daten zu verarbeiten. Bei einigen MFTs kann die asynchrone Verarbeitung effizienter sein. Es ist jedoch auch komplexer, Sie zu implementieren.<br/> Weitere Informationen finden Sie unter <a href="asynchronous-mfts.md">asynchrone MFTs</a>.<br/></td>
</tr>
<tr class="odd">
<td>Raten Steuerung, Trick Modus oder umgekehrte Wiedergabe</td>
<td>Siehe <a href="implementing-rate-control.md">Implementieren der Raten Kontrolle</a>.</td>
</tr>
<tr class="even">
<td>Wenn Ihr MFT Threads erstellt...</td>
<td>Implementieren Sie die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>imfrealtimeclient</strong></a> -Schnittstelle.</td>
</tr>
<tr class="odd">
<td>Wenn Ihr MFT über Lizenzierungs Einschränkungen verfügt...</td>
<td>Verwenden Sie ggf. den Feld-of-use-Mechanismus. Siehe <a href="field-of-use-restrictions.md">Einschränkungen für Felder</a>.</td>
</tr>
<tr class="even">
<td>Wenn Sie ein vorhandenes DirectX-Medienobjekt (DMO) portieren...</td>
<td>Weitere Informationen finden Sie <a href="comparison-of-mfts-and-dmos.md">unter Vergleich von MFTs und DMOS</a>.</td>
</tr>
</tbody>
</table>



 

Dieser Abschnitt enthält die folgenden Themen:

-   [Zeitstempel und Dauer](time-stamps-and-durations.md)
-   [Verarbeiten von streamänderungen](handling-stream-changes.md)
-   [Implementieren eines Codec-MFT](implementing-a-codec-mft.md)
-   [Direct3D-kompatible MFTs](direct3d-aware-mfts.md)
-   [Hardware-MFTs](hardware-mfts.md)
-   [Codec-Verdienst](codec-merit.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 




