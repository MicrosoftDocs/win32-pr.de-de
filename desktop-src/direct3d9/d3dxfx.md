---
description: Optionen zum Speichern und Erstellen von Effekten.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995077"
---
# <a name="d3dxfx"></a>D3DXFX

Optionen zum Speichern und Erstellen von Effekten.

Die Konstanten in der folgenden Tabelle sind in d3dx9effect.h definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Effect State Save and Restore Flags</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> oder restored beim Aufrufen von End wird kein Zustand <a href="id3dxeffect--end.md"><strong>gespeichert.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Ein StateBlock speichert den Zustand beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin und</strong></a> stellt den Zustand beim Aufrufen von End wieder <a href="id3dxeffect--end.md"><strong>wieder auf.</strong></a></td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Ein Zustandsblock speichert den Zustand (mit Ausnahme von Shadern und Shaderkonstatoren) beim Aufrufen von <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> und stellt den Zustand beim Aufrufen von <a href="id3dxeffect--end.md"><strong>End wieder auf.</strong></a></td>
</tr>
<tr class="odd">
<td>Flags für die Effekterstellung</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>Der Effekt ist nicht klonbar und enthält keine binären Shaderdaten. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc gibt</strong></a> keine Shaderfunktionszeige zurück. Durch festlegen dieses Flags wird die Arbeitsspeicherauslastung um etwa 50 % reduziert, da das Effektsystem keine Kopie der Shader im Arbeitsspeicher behalten muss. Dieses Flag wird von <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect,</strong></a> <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>und <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource verwendet.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Ermöglicht die Zuordnung einer Effektressource in den Adressraum des Uppders eines Computers. Eine wichtige Einschränkung besteht darin, dass Zeichenfolgen und Handles nicht austauschbar verwendet werden können. Das folgende Beispiel würde nicht mehr funktionieren. <span data-codelanguage=""></span>
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

Stattdessen muss eine Methode wie [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) verwendet werden, um das Handle des Parameters zu speichern, der dann zum Übergeben von Variablen an den Effekt verwendet wird.</td>
</tr>
</tbody>
</table>



 

Die Konstanten in der folgenden Tabelle sind nicht standardmäßig definiert und müssen vom Entwickler definiert werden.



| Effect Preprocessor \# define es | BESCHREIBUNG                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXFX \_ \_ LARGEADDRESS-HANDLE   | Definieren Sie diesen Wert, bevor Sie d3dx9.h einschließen, damit ihre Anwendung beim Versuch, Zeichenfolgen an D3DXHANDLE-Parameter zu übergeben, nicht kompiliert werden kann. Dadurch wird sichergestellt, dass gültige Informationen an die Laufzeit übergeben werden. |
| Effektlinkerflags            | BESCHREIBUNG                                                                                                                                                                                                                          |
| LARGE \_ ADDRESS \_ AWARE          | Wenn Sie das Linkerflag LARGE ADDRESS AWARE = 1 festlegen, \_ kann die Anwendung Bei Bedarf Ressourcen über den Grenzwert von \_ 2 GB an Adressen zuordnen.                                                                                      |



 

Das Effektsystem verwendet Zustandsblöcke, um den Zustand automatisch zu speichern und wiederherzustellen. Weitere Informationen zu Zustandsblöcken finden Sie unter [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9).](state-blocks-save-and-restore-state.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektkonstanten](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



