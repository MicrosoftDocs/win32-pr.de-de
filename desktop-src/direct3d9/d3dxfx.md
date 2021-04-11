---
description: Optionen zum Speichern und Erstellen von Effekten.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123386"
---
# <a name="d3dxfx"></a>D3DXFX

Optionen zum Speichern und Erstellen von Effekten.

Die Konstanten in der folgenden Tabelle sind in d3dx9effect. h definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Speicher-und Wiederherstellungs Flags des Wirkungs Zustands</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Beim Aufrufen von " <a href="id3dxeffect--end.md"><strong>End</strong></a>" <a href="id3dxeffect--begin.md"><strong>oder "</strong></a> wieder hergestellt" wird kein Status gespeichert.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Ein stateblock speichert den Zustand beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End</strong></a>wieder her.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Ein stateblock speichert den Zustand (außer Shader und shaderkonstanten) beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End</strong></a>wieder her.</td>
</tr>
<tr class="odd">
<td>Effekte erstellungsflags</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>Der Effekt ist nicht klonbar und enthält keine Shader-Binärdaten. <a href="id3dxbaseeffect--getpassdesc.md"><strong>Getpassde SC</strong></a> gibt keine shaderfunktionszeiger zurück. Wenn Sie dieses Flag festlegen, wird die Arbeitsspeicher Auslastung um etwa 50% reduziert, da das Effektsystem nicht mehr benötigt, um eine Kopie der Shader im Arbeitsspeicher beizubehalten. Dieses Flag wird von <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>und <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>verwendet.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Ermöglicht die Zuordnung einer Effekt Ressource in den uppder-Adressraum eines Computers. Eine wichtige Einschränkung ist, dass Sie Zeichen folgen und Handles nicht austauschbar verwenden können. Beispielsweise würde Folgendes nicht mehr funktionieren. <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

Stattdessen muss eine Methode wie z. b. [<strong>getparameterbyname</strong>](id3dxbaseeffect--getparameterbyname.md) verwendet werden, um das Handle des-Parameters zu speichern, das dann verwendet wird, um Variablen an den Effekt zu übergeben.</td>
</tr>
</tbody>
</table>



 

Die Konstanten in der folgenden Tabelle sind nicht standardmäßig definiert und müssen vom Entwickler definiert werden.



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Effekt \# Präprozessordefinition | BESCHREIBUNG                                                                                                                                                                                                                          |
| D3DXFX \_ largeaddress- \_ handle   | Definieren Sie diesen Wert, bevor Sie d3dx9. h einschließen, damit die Anwendung nicht kompiliert werden kann, wenn Sie versuchen, Zeichen folgen an D3DXHANDLE-Parameter zu übergeben. Dadurch wird sichergestellt, dass gültige Informationen an die Laufzeit übermittelt werden. |
| Effekt-Linker-Flags            | BESCHREIBUNG                                                                                                                                                                                                                          |
| hohe \_ Adressen \_ Unterstützung          | Wenn Sie das Linker-Flag "große Adressen" festlegen \_ \_ = 1, kann die Anwendung bei Bedarf Ressourcen über dem Adress Limit von 2 GB zuordnen.                                                                                      |



 

Das Effektsystem verwendet Zustands Blöcke zum automatischen Speichern und Wiederherstellen des Zustands. Weitere Informationen zu Status Blöcken finden Sie unter [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Konstanten](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



