---
description: Der DVD-Kopierschutz-Eigenschaftensatz ermöglicht die Authentifizierung von Kopierschutzinformationen von Hardware- oder Softwareentschlüsselern. Verwenden Sie diesen Eigenschaftensatz, um nicht autorisiertes Kopieren von vorab aufgezeichneten DVD-Video-Dateien zu verhindern.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD-Kopierschutz-Eigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76034c0ac9b310d446f142d31b96ea2edbe6b725
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477347"
---
# <a name="dvd-copy-protection-property-set"></a>DVD Copy Protection-Eigenschaftensatz

Der DVD-Kopierschutz-Eigenschaftensatz ermöglicht die Authentifizierung von Kopierschutzinformationen von Hardware- oder Softwareentschlüsselern. Verwenden Sie diesen Eigenschaftensatz, um nicht autorisiertes Kopieren von vorab aufgezeichneten DVD-Video-Dateien zu verhindern.

Microsoft stellt Software zur Verfügung, die den für das Verschlüsselungsschema erforderlichen Authentifizierungsprozess vereinfacht, wodurch ein DVD-ROM-Laufwerk zum Authentifizieren und Übertragen von Schlüsseln mit einem DVD-Entschlüsselungsprogramm aktiviert wird. Microsoft hat derzeit keine Pläne für den Versand einer DVD-Entschlüsselungsvorrichtung und stellt stattdessen Betriebssystemcode zur Verfügung, der als Agent für die Authentifizierung von Hardware- oder Softwareentschlüsselern fungieren soll.

Der DVD-Navigator initiiert und steuert den Schlüsselaustauschprozess. Der DVD-Minitreiber muss nur die folgenden Eigenschaften implementieren. Andere Komponenten verarbeiten den Rest.

Jeder DVD-Eingabestream erhält Kopierschutzeigenschaften. Dies gilt auch, wenn dieselbe Hardware alle DVD-Streams steuert.

Die folgenden Informationen stellen die erforderlichen Konstanten und Datentypen für diesen Eigenschaftssatz in Aufrufen von [**IKsPropertySet-Methoden**](ikspropertyset.md) vor. Sie stellt Werte für die **Parameter GUID** (*guidPropSet),* Eigenschaften-ID (*dwPropID*) und Eigenschaftsdatentyp (*pPropData*) zur Anwendung.



| Bezeichnung | Wert |
|-------------------|---------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ CopyProt |



 




| Eigenschafts-ID | BESCHREIBUNG | 
|-------------|-------------|
| <a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a> | Fragt ab, ob es sich bei der Videoausgabe um videobasierte Standarddefinitionen handelt, analoges Komponentenvideo. | 
| AM_PROPERTY_COPY_MACROVISION | Dies ist eine eigenschaft, die nur festgelegt ist. Diese Eigenschaft legt die Schutzebene für analoge Kopierdaten für den NTSC-Encoder am Ausgabeende des Empfangspins fest. Verwendet <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>. | 
| AM_PROPERTY_DVDCOPY_CHLG_KEY | Sowohl Get- als auch Set-Vorgänge werden für diese Eigenschaft unterstützt. Ein get-Vorgang fordert den Decoder auf, seinen Bus-Challenge-Schlüssel zur Verfügung zu stellen. Ein Set-Vorgang stellt dem Decoder den Bus-Challenge-Schlüssel aus dem DVD-Laufwerk zurEntschlüsselung. Die in dieser Eigenschaft übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY.</strong></a> | 
| AM_PROPERTY_DVDCOPY_DEC_KEY2 | Dies ist eine get-only-Eigenschaft. Diese Eigenschaft fordert an, dass der Busschlüssel 2 des Decoders auf das DVD-Laufwerk übertragen wird. Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY.</strong></a> | 
| AM_PROPERTY_DVDCOPY_DISC_KEY | Eigenschaft "Nur festlegen". Dadurch wird ein Datenträgerschlüssel (Disk Key) ermöglicht. Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY.</strong></a> | 
| AM_PROPERTY_DVDCOPY_DVD_KEY1 | Dies ist eine eigenschaft, die nur festgelegt ist. Diese Eigenschaft stellt den DVD-Laufwerksbusschlüssel 1 für den Decoder zurt. Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY.</strong></a> | 
| AM_PROPERTY_DVDCOPY_REGION | Der Regioncode fordert die Vom DVD-Konsortium definierte Regiondefinition an, in der der Decoder wieder verwendet werden darf. Dieser Bereich wird als <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> definiert. | 
| AM_PROPERTY_DVDCOPY_SET_COPY_STATE | Sowohl get als auch set werden für diese Eigenschaft unterstützt. Get wird zuerst aufgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist. Die festgelegten Eigenschaften sind Hinweise darauf, in welcher Phase der Kopierschutzaushandlung der Filter eintritt. Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE.</strong></a> | 
| AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT | Wenn diese Eigenschaft <strong>TRUE ist,</strong>sendet der DVD-Navigator keine AM_UseNewCSSKey <strong>vor</strong> dem Aushandeln des Datenträgerschlüssels. Siehe <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br /> Schreibgeschützt. Die Eigenschaftsdaten sind ein <strong>BOOL-Wert.</strong><br /><blockquote>[!Note]<br />Gilt für Windows 7.</blockquote><br /> | 
| AM_PROPERTY_DVDCOPY_TITLE_KEY | Dies ist eine eigenschaft, die nur festgelegt ist. Dies stellt den Titelschlüssel aus dem aktuellen Inhalt zur Lage. Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY.</strong></a> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




