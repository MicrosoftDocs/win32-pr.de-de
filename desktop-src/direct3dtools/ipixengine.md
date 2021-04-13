---
description: Ursprüngliche Schnittstelle für die Kommunikation von Daten über einen vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipixengine-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482643"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span id="vspixengine.ipixengine"></span>Ipixengine-Schnittstelle

Ursprüngliche Schnittstelle für die Kommunikation von Daten über einen vsglog.

## <a name="members"></a>Member

Die **ipixengine** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ipixengine** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **ipixengine** -Schnittstelle verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></td><td style="text-align: left;"><p>Öffnet ein Grafik Protokoll.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>Runexperiment</strong></a></td><td style="text-align: left;"><p>Führt ein Experiment aus.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></td><td style="text-align: left;"><p>Speichert das Grafik Protokoll an der angegebenen Position.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParser-Prozess</strong></a></td><td style="text-align: left;"><p>Nicht verwendet.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Abschlusses</strong></a></td><td style="text-align: left;"><p>Fährt die Engine herunter.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
