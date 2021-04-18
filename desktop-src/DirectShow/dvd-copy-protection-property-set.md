---
description: Der Eigenschaften Satz "DVD-Kopierschutz" ermöglicht die Authentifizierung von Informationen zum Kopierschutz von Hardware-oder Software Entschlüsselungs Informationen. Verwenden Sie diesen Eigenschaften Satz, um das nicht autorisierte Kopieren von DVD-Videos zu verhindern.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD-Kopierschutz-Eigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361649"
---
# <a name="dvd-copy-protection-property-set"></a>Eigenschaften Satz für den DVD-Kopierschutz

Der Eigenschaften Satz "DVD-Kopierschutz" ermöglicht die Authentifizierung von Informationen zum Kopierschutz von Hardware-oder Software Entschlüsselungs Informationen. Verwenden Sie diesen Eigenschaften Satz, um das nicht autorisierte Kopieren von DVD-Videos zu verhindern.

Microsoft stellt Software zur Verfügung, die den für das Verschlüsselungsschema erforderlichen Authentifizierungsprozess vereinfacht, sodass ein DVD-ROM-Laufwerk Schlüssel mit einer DVD-Entschlüsselung authentifizieren und übertragen kann. Microsoft ist nicht in der Lage, eine DVD-Entschlüsselung zu senden und stellt stattdessen Betriebssystem Code bereit, der als Agent fungiert, um die Authentifizierung von Hardware-oder Software Entschlüsselungs Optionen zu aktivieren.

Der DVD-Navigator initiiert und steuert den Schlüsselaustausch Vorgang. Der DVD-Mini Treiber muss lediglich die folgenden Eigenschaften implementieren. Andere Komponenten verarbeiten den Rest.

Jeder DVD-Eingabestream erhält Kopierschutz Eigenschaften. Dies gilt auch, wenn dieselbe Hardware alle DVD-Streams steuert.

Die folgenden Informationen stellen die erforderlichen Konstanten und Datentypen dar, die für diesen Eigenschaften Satz in Aufrufen von " [**ikspropertyset**](ikspropertyset.md) "-Methoden verwendet werden. Es werden Werte für die Parameter **GUID** (*guidpropset*), Property ID (*dwpropid*) und Property Data Type (*ppropdata*) bereitstellt.



|                   |                           |
|-------------------|---------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropsetid \_ copyprot |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschafts-ID</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></td>
<td>Fragt ab, ob es sich bei der Videoausgabe um ein Video mit der standardmäßigen Definition, Analog</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_COPY_MACROVISION</td>
<td>Dies ist eine Eigenschaft, die nur festgelegt ist. Diese Eigenschaft legt die Ebene des analogen Kopierschutzes für den NTSC-Encoder am Ausgabe Ende der empfangenden PIN fest. Verwendet <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_CHLG_KEY</td>
<td>Sowohl Get-als auch Set-Vorgänge werden für diese Eigenschaft unterstützt. Mit einem Get-Vorgang wird der Decoder aufgefordert, seinen busaufforderungs Schlüssel bereitzustellen. Durch einen Set-Vorgang erhält der Decoder den Bus Challenge-Schlüssel vom DVD-Laufwerk. Bei den in dieser Eigenschaft bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DEC_KEY2</td>
<td>Dabei handelt es sich um eine reine Get-Eigenschaft. Diese Eigenschaft fordert an, dass der buskkey 2 des Decoders auf das DVD-Laufwerk übertragen werden soll. Bei den bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_DISC_KEY</td>
<td>Eigenschaft, die nur festgelegt ist. Dies stellt einen Disc-Schlüssel bereit. Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DVD_KEY1</td>
<td>Dies ist eine Eigenschaft, die nur festgelegt ist. Diese Eigenschaft stellt dem Decoder den DVD-laufwerkbus Schlüssel 1 zur Verfügung. Bei den bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_REGION</td>
<td>Der Regions Code fordert die Regions Definition an, in der der Decoder durch das DVD-Konsortium definiert werden darf. Diese Region ist als <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> Struktur definiert.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_SET_COPY_STATE</td>
<td>"Get" und "Set" werden für diese Eigenschaft unterstützt. Get wird zuerst aufgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist. Die Set-Eigenschaften sind Hinweise darauf, in welcher Phase der Kopierschutz Aushandlung der Filter eintritt. Bei den bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</td>
<td>Wenn diese Eigenschaft den Wert <strong>true</strong>hat, sendet der DVD-Navigator vor dem Aushandeln des CD-Schlüssels keine <strong>AM_UseNewCSSKey</strong> Samples. Siehe <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br/> Schreibgeschützt. Die Eigenschaften Daten sind ein <strong>boolescher</strong> Wert.<br/>
<blockquote>
[!Note]<br />
Gilt für Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_TITLE_KEY</td>
<td>Dies ist eine Eigenschaft, die nur festgelegt ist. Dadurch wird der Titel Schlüssel aus dem aktuellen Inhalt bereitstellt. Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




