---
description: Der Dvd Copy Protection-Eigenschaftensatz ermöglicht die Authentifizierung von Kopierschutzinformationen von Hardware- oder Softwareentschlüsselern. Verwenden Sie diesen Eigenschaftensatz, um zu verhindern, dass nicht autorisierte Kopien von vorab aufgezeichneten DVD-Videos erstellt werden.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD-Kopierschutz-Eigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909478"
---
# <a name="dvd-copy-protection-property-set"></a>DVD Copy Protection-Eigenschaftensatz

Der Dvd Copy Protection-Eigenschaftensatz ermöglicht die Authentifizierung von Kopierschutzinformationen von Hardware- oder Softwareentschlüsselern. Verwenden Sie diesen Eigenschaftensatz, um zu verhindern, dass nicht autorisierte Kopien von vorab aufgezeichneten DVD-Videos erstellt werden.

Microsoft stellt Software bereit, die den für das Verschlüsselungsschema erforderlichen Authentifizierungsprozess erleichtert, sodass ein DVD-ROM-Laufwerk Schlüssel mit einem DVD-Entschlüsselungsprogramm authentifizieren und übertragen kann. Microsoft bietet derzeit keine DVD-Entschlüsseler an und stellt stattdessen Betriebssystemcode bereit, der als Agent fungiert, um die Authentifizierung von Hardware- oder Softwareentschlüsselern zu ermöglichen.

Der DVD-Navigator initiiert und steuert den Schlüsselaustauschprozess. Der DVD-Minitreiber muss nur die folgenden Eigenschaften implementieren. Andere Komponenten verarbeiten den Rest.

Jeder DVD-Eingabestream empfängt Kopierschutzeigenschaften. Dies gilt auch, wenn die gleiche Hardware alle DVD-Streams steuert.

Die folgenden Informationen enthalten die erforderlichen Konstanten und Datentypen, die für diesen Eigenschaftensatz in Aufrufen von [**IKsPropertySet-Methoden**](ikspropertyset.md) verwendet werden sollen. Sie stellt Werte für die **Parameter GUID** (*guidPropSet),* Eigenschaften-ID (*dwPropID*) und Eigenschaftendatentyp (*pPropData*) bereit.



| Bezeichnung | Wert |
|-------------------|---------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ CopyProt |



 



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
<td>Fragt ab, ob es sich bei der Videoausgabe um ein Analogkomponentenvideo mit Standarddefinition handelt.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_COPY_MACROVISION</td>
<td>Dies ist eine eigenschaft, die nur festgelegt ist. Diese Eigenschaft legt die analoge Kopierschutzebene für den NTSC-Encoder am Ausgabeende des empfangenden Pins fest. Verwendet <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_CHLG_KEY</td>
<td>Sowohl Get- als auch Set-Vorgänge werden für diese Eigenschaft unterstützt. Ein Get-Vorgang fordert den Decoder auf, seinen Bus-Challenge-Schlüssel zur Verfügung zu stellen. Ein Set-Vorgang stellt dem Decoder den Bus-Challenge-Schlüssel aus dem DVD-Laufwerk zurEntschlüsselung. Die in dieser Eigenschaft übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY.</strong></a></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DEC_KEY2</td>
<td>Dies ist eine get-only-Eigenschaft. Diese Eigenschaft fordert an, dass der Busschlüssel 2 des Decoders auf das DVD-Laufwerk übertragen wird. Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY.</strong></a></td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_DISC_KEY</td>
<td>Eigenschaft "Nur festlegen". Dadurch wird ein Datenträgerschlüssel (Disk Key) ermöglicht. Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY.</strong></a></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DVD_KEY1</td>
<td>Dies ist eine eigenschaft, die nur festgelegt ist. Diese Eigenschaft stellt den DVD-Laufwerksbusschlüssel 1 für den Decoder zurt. Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY.</strong></a></td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_REGION</td>
<td>Der Regioncode fordert die Vom DVD-Konsortium definierte Regiondefinition an, in der der Decoder wieder verwendet werden darf. Dieser Bereich wird als <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION-Struktur</strong></a> definiert.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_SET_COPY_STATE</td>
<td>Sowohl get als auch set werden für diese Eigenschaft unterstützt. Get wird zuerst aufgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist. Die festgelegten Eigenschaften sind Hinweise darauf, in welche Phase der Kopierschutzaushandlung der Filter eintritt. Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</td>
<td>Wenn diese Eigenschaft <strong>TRUE</strong>ist, sendet der DVD-Navigator vor dem Aushandeln des Datenträgerschlüssels keine <strong>AM_UseNewCSSKey</strong> Beispiele. Weitere Informationen finden Sie <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>unter AM_SAMPLE2_PROPERTIES</strong></a>.<br/> Schreibgeschützt. Die Eigenschaftsdaten sind ein <strong>BOOL-Wert.</strong><br/>
<blockquote>
[!Note]<br />
Gilt für Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_TITLE_KEY</td>
<td>Dies ist eine eigenschaft, die nur festgelegt ist. Dadurch wird der Titelschlüssel aus dem aktuellen Inhalt zur Verfügung stellen. Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




