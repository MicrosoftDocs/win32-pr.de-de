---
description: Optionen zum Speichern und Erstellen von Effekten.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6858f659b1561a526a284b3ea2dca0e1d9a11a31
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624086"
---
# <a name="d3dxfx"></a>D3DXFX

Optionen zum Speichern und Erstellen von Effekten.

Die Konstanten in der folgenden Tabelle sind in d3dx9effect.h definiert.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Flags zum Speichern und Wiederherstellen des Effect-Zustands</td>
<td>Beschreibung</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> oder beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End</strong></a>wird kein Zustand gespeichert.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Ein Zustandsblock speichert den Zustand beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End</strong></a>wieder her.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Ein Zustandsblock speichert den Zustand (mit Ausnahme von Shadern und Shaderkonstanten) beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End</strong></a>wieder her.</td>
</tr>
<tr class="odd">
<td>Flags für die Effekterstellung</td>
<td>Beschreibung</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>Der Effekt ist nicht klonbar und enthält keine binären Shaderdaten. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> gibt keine Shaderfunktionszeiger zurück. Durch Festlegen dieses Flags wird die Speicherauslastung um etwa 50 % reduziert, da das Effektsystem keine Kopie der Shader im Arbeitsspeicher speichern muss. Dieses Flag wird von <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect,</strong></a> <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>und <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>verwendet.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Aktiviert die Zuordnung einer Effektressource in den Uppder-Adressraum eines Computers. Eine wichtige Einschränkung besteht darin, dass Sie keine Zeichenfolgen und Handles austauschbar verwenden können. Das folgende Beispiel würde nicht mehr funktionieren. <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

Stattdessen muss eine Methode wie [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) verwendet werden, um das Handle des Parameters zu speichern, der dann zum Übergeben von Variablen an den Effekt verwendet wird.</td>
</tr>
</tbody>
</table>



 

Die Konstanten in der folgenden Tabelle sind nicht standardmäßig definiert und müssen vom Entwickler definiert werden.



| Effect Preprocessor \# define es | Beschreibung                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXFX \_ \_ LARGEADDRESS-HANDLE   | Definieren Sie diesen Wert, bevor Sie d3dx9.h einschließen, damit Ihre Anwendung beim Versuch, Zeichenfolgen an D3DXHANDLE-Parameter zu übergeben, nicht kompiliert werden kann. Dadurch wird sichergestellt, dass gültige Informationen an die Laufzeit übergeben werden. |
| Effektlinkerflags            | Beschreibung                                                                                                                                                                                                                          |
| LARGE \_ ADDRESS \_ AWARE          | Wenn Sie das Linkerflag LARGE ADDRESS AWARE = 1 festlegen, \_ kann die Anwendung bei Bedarf Ressourcen über den Grenzwert von \_ 2 GB an Adressen zuordnen.                                                                                      |



 

Das Effektsystem verwendet Zustandsblöcke, um den Zustand automatisch zu speichern und wiederherzustellen. Weitere Informationen zu Zustandsblöcken finden Sie unter [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9).](state-blocks-save-and-restore-state.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektkonstanten](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



