---
description: Die folgenden Enumerationen werden in vspixengine.h deklariert.
MS-HAID: vspixengine.vspixengine\_enumerations
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Direct3D-Diagnose – Erfassungsschnittstellenenumerationen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: A67402DE-8CBF-470A-97B4-3CF531731F24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 94b5e656a1012f8b48cd4fbc34f34d94a145872d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626166"
---
# <a name="span-idvspixenginevspixengine_enumerationsspandirect3d-diagnostics-capture-interface-enumerations"></a><span id="vspixengine.vspixengine_enumerations"></span>Erfassungsschnittstellenenumerationen der Direct3D-Diagnose

Die folgenden Enumerationen werden in vspixengine.h deklariert.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In diesem Abschnitt

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Thema</th><th>Beschreibung</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/xml-resource-ids"><strong>Xml_Resource_Ids</strong></a></p></td><td><p>Vom Aufrufer festgelegte Ressourcenzeichenfolgen-IDs, die in XML-Daten zum Visualisieren von Objekten zurückgegeben werden sollen</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/resource-id"><strong>Resource_Id</strong></a></p></td><td><p>Definiert Ressourcen-IDs für freigegebene Zeichenfolgenressourcen. Diese werden vom Host an die Erfassungs-Engine übergeben. Sie werden verwendet, um Zeichenfolgen in der HUD-Überlagerung der erfassten App anzuzeigen oder Registrierungswerte von Visual Studio Optionen an die Erfassungs-ENGI zu übergeben.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/hresult"><strong>Hresult</strong></a></p></td><td><p>Benutzerdefinierte HRESULT-Werte für die Grafikdiagnose-Erfassungsschnittstelle.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/remotecommandtype"><strong>RemoteCommandType</strong></a></p></td><td><p>Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/callbackcommandtype"><strong>CallbackCommandType</strong></a></p></td><td><p>Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixpiperesponse"><strong>PixPipeResponse</strong></a></p></td><td><p>Eine Enumeration, die zum Senden von Antworten von der Erfassungs-Engine an Grafikdiagnose verwendet wird.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/remotingversion"><strong>REMOTINGVERSION</strong></a></p></td><td><p>Eine Enumeration, mit der angegeben wird, welche Version des Remoting-Protoculs verwendet wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelkillreason"><strong>PIXELKILLREASON</strong></a></p></td><td><p>Eine Enumeration, die angibt, warum ein Pixel abgelehnt wurde.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryflags"><strong>PIXELHISTORYFLAGS</strong></a></p></td><td><p>Eine Enumeration, die Flags enthält, die verwendet werden, um ein Pixelverlaufsergebnis zu beschreiben. Weitere Informationen finden Sie unter PixelHistoryOperation.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/eventcolumnid"><strong>EVENTCOLUMNID</strong></a></p></td><td><p>Eine Enumeration, mit der bekannte Spalten-IDs angegeben werden. Hierbei handelt es sich um Spalten-IDs, die von allen Implementierungen unterstützt werden sollen.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/objectstatetype"><strong>OBJECTSTATETYPE</strong></a></p></td><td><p>Intern</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/objecttablecolumnid"><strong>OBJECTTABLECOLUMNID</strong></a></p></td><td><p>Eine Enumeration, mit der Eigenschaften von Daten angegeben werden, die von einer Objekttabellenanforderung zurückgegeben werden. Weitere Informationen finden Sie unter IObjectTableRequest.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestages"><strong>PIPELINESTAGES</strong></a></p></td><td><p>Eine Enumeration, mit der eine Phase der Grafikpipeline angegeben wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/checksumalgorithm"><strong>CHECKSUMALGORITHM</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um den zu verwendenden Prüfsummenalgorithmus anzugeben.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/eventtype"><strong>EVENTTYPE</strong></a></p></td><td><p>Eine Enumeration, mit der der Typ eines Ereignisses angegeben wird.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-header-columns"><strong>DESCRIPTOR_HEAP_HEADER_COLUMNS</strong></a></p></td><td><p>Eine Enumeration, mit der ein Coumn-Header im Deskriptorheap-Viewer angegeben wird</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-columns"><strong>DESCRIPTOR_HEAP_COLUMNS</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um eine Spalte im Deskriptorheap-Viewer anzugeben.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttype"><strong>EXPERIMENTTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/dumpertype"><strong>DUMPERTYPE</strong></a></p></td><td><p>Eine Enumeration, mit der angegeben wird, welcher Puffertyp IGenericBufferDataRequest zurückgibt.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttriggertype"><strong>EXPERIMENTTRIGGERTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/register-format"><strong>REGISTER_FORMAT</strong></a></p></td><td><p>Intern</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/primitive-topology"><strong>PRIMITIVE_TOPOLOGY</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um die Topologie eines Gitternetzes anzugeben. Siehe MeshDataVertCallback.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysisstage"><strong>OFFLINEANALYSISSTAGE</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um Phasen des Fortschritts in der Frameanalyse anzugeben.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysissource"><strong>OFFLINEANALYSISSOURCE</strong></a></p></td><td><p>Eine Enumeration, die verwendet wird, um die Quelle der Grafikinformationen für die Frameanalyse anzugeben.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Verwandte Themen

[Direct3D Diagnostics Capture Interface Reference](vspixengine-reference.md)

 

 
