---
description: Multimedia-Streaming-Objekte
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Multimedia-Streaming-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351688"
---
# <a name="multimedia-streaming-objects"></a>Multimedia-Streaming-Objekte

> [!Note]  
> Diese API ist veraltet. Diese sollten von neuen Anwendungen nicht verwendet werden.

 

In der folgenden Tabelle werden die multimediastreaming-Objekte beschrieben.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>CLSID</th>
<th>BESCHREIBUNG</th>
<th>Unterstützte Schnittstellen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CLSID_AMMediaTypeStream</td>
<td>Kann für jeden von DirectShow unterstützten Datentyp Medien Beispiele erstellen.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>Iammediastream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>Imediastream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMAudioData</td>
<td>Implementierung des <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>iaudiodata</strong></a> -audiocontainerobjekts.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>Iaudiodata</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_AMDirectDrawStream</td>
<td>DirectDraw-Mediendaten Strom, der einem DirectShow Multimedia-Stream hinzugefügt werden kann.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>Iammediastream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>Imediastream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>Idirectdrawmediastream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMMultiMediaStream</td>
<td>DirectShow-Implementierung von Multimedia-Stream.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>Iammultimediastream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>Imultimediastream</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_MediaStreamFilter</td>
<td>Stellt über die <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>iammultimediastream</strong></a> -Schnittstelle multimediastreaming-Funktionen für das CLSID_AMMultiMediaStream Objekt bereit.</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>–</td>
<td>Beispiele, die vom CLSID_AMMediaTypeStream-Objekt erstellt wurden.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>Istreamsample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>Imediasample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>–</td>
<td>Beispiele, die vom DirectDraw-Stream erstellt wurden.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>Istreamsample</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>Idirectdrawstreamsample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>Imediasample</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



