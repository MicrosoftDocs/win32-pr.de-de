---
description: Die folgenden Enumerationen werden in "vspixengine. h" deklariert.
MS-HAID: vspixengine.vspixengine\_enumerations
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Direct3D Diagnostics Capture Interface-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: A67402DE-8CBF-470A-97B4-3CF531731F24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 059f91aa806afd60d5efe755d015495eb2f445f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344578"
---
# <a name="span-idvspixenginevspixengine_enumerationsspandirect3d-diagnostics-capture-interface-enumerations"></a><span id="vspixengine.vspixengine_enumerations"></span>Direct3D Diagnostics Capture Interface-Enumerationen

Die folgenden Enumerationen werden in "vspixengine. h" deklariert.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In diesem Abschnitt

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Thema</th><th>BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/xml-resource-ids"><strong>Xml_Resource_Ids</strong></a></p></td><td><p>Vom Aufrufer festgelegte Ressourcen Zeichen folgen-IDs, die in XML-Daten zum Visualisieren von Objekten zurückgegeben</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/resource-id"><strong>Resource_Id</strong></a></p></td><td><p>Definiert Ressourcen-IDs für freigegebene Zeichen folgen Ressourcen. Diese werden vom Host an die Aufzeichnungs-Engine übermittelt. Sie werden verwendet, um Zeichen folgen für die HUD-Überlagerung der erfassten App anzuzeigen oder um Registrierungs Werte von Visual Studio-Optionen an die Erfassungs Engi zu übergeben.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/hresult"><strong>HRESULT</strong></a></p></td><td><p>Benutzerdefinierte HRESULT-Werte für die Schnittstelle zur Grafik Diagnose Erfassung.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/remotecommandtype"><strong>Remotecommandtype</strong></a></p></td><td><p>Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/callbackcommandtype"><strong>Callbackcommandtype</strong></a></p></td><td><p>Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixpiperesponse"><strong>Pixpiperesponse</strong></a></p></td><td><p>Eine Enumeration, mit der Antworten von der Aufzeichnungs-Engine an Grafikdiagnose gesendet werden.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/remotingversion"><strong>Remotingversion</strong></a></p></td><td><p>Eine-Aufzählung, die verwendet wird, um anzugeben, welche Version des Remoting-Protos verwendet wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelkillreason"><strong>Pixelkillreason</strong></a></p></td><td><p>Eine-Aufzählung, mit der angegeben wird, warum ein Pixel abgelehnt wurde.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryflags"><strong>Pixelhistoryflags</strong></a></p></td><td><p>Eine Enumeration, die Flags enthält, die zum Beschreiben eines Pixel Verlaufs Ergebnisses verwendet werden. Siehe pixelhistoryoperation.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/eventcolumnid"><strong>Eventcolumnid</strong></a></p></td><td><p>Eine-Aufzählung, mit der bekannte Spalten-IDs angegeben werden. Dies sind Spalten-IDs, die von allen-Implementierungen unterstützt werden.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/objectstatetype"><strong>Objectstatuetype</strong></a></p></td><td><p>Intern</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/objecttablecolumnid"><strong>Objecttablecolumnid</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um die Eigenschaften der von einer Objekt Tabellen Anforderung zurückgegebenen Daten anzugeben. Weitere Informationen finden Sie unter iobjecttablerequest.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestages"><strong>Pipelinestages</strong></a></p></td><td><p>Eine-Aufzählung, die zum Angeben einer Stufe der Grafik Pipeline verwendet wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/checksumalgorithm"><strong>Checksumalgorithm</strong></a></p></td><td><p>Eine-Aufzählung, die verwendet wird, um den zu verwendenden Prüfsummen Algorithmus anzugeben.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/eventtype"><strong>EventType</strong></a></p></td><td><p>Eine-Aufzählung, mit der der Typ eines Ereignisses angegeben wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-header-columns"><strong>DESCRIPTOR_HEAP_HEADER_COLUMNS</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um einen Spalte-Header im deskriptorheap-Viewer anzugeben.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-columns"><strong>DESCRIPTOR_HEAP_COLUMNS</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um eine Spalte im deskriptorheap-Viewer anzugeben.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttype"><strong>Experimentstyp</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/dumpertype"><strong>Dumpertype</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um anzugeben, welcher Puffertyp von igenericbufferdatarequest zurückgegeben wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttriggertype"><strong>Experimenttriggertype</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/register-format"><strong>REGISTER_FORMAT</strong></a></p></td><td><p>Intern</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/primitive-topology"><strong>PRIMITIVE_TOPOLOGY</strong></a></p></td><td><p>Eine-Aufzählung, die zur Angabe der Topologie eines Netzes verwendet wird. Weitere Informationen finden Sie unter meshdatavertcallback.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysisstage"><strong>Offlineanalysisstage</strong></a></p></td><td><p>Eine Enumeration, mit der Phasen des Fortschritts in der Frame-Analyse angegeben werden.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysissource"><strong>Offlineanalysissource</strong></a></p></td><td><p>Eine Enumeration, die die Quelle von Grafik Informationen für die Frame-Analyse angibt.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Verwandte Themen

[Direct3D Diagnostics Capture Interface-Referenz](vspixengine-reference.md)

 

 
