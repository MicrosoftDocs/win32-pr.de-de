---
description: Gibt an, wie die Medien Sitzung ein Objekt in der Topologie herunterfährt.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: MF_TOPONODE_NOSHUTDOWN_ON_REMOVE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345786"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>MF \_ toponode \_ noshutdown \_ beim \_ Remove-Attribut

Gibt an, wie die Medien Sitzung ein Objekt in der Topologie herunterfährt.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für die folgenden Typen von topologietknoten:

-   Ausgabe Knoten
-   Ein beliebiger Transformations Knoten, der eine *asynchrone* Media Foundation Transformation (MFT) enthält.

Das-Attribut kann die folgenden Werte aufweisen:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TRUE</strong></td>
<td>Wenn die Medien Sitzung zu einer neuen Topologie wechselt oder die aktuelle Topologie löscht, wird das Objekt, das zu diesem topologieknoten gehört, nicht heruntergefahren.</td>
</tr>
<tr class="even">
<td><strong>FALSE</strong></td>
<td>Wenn die Medien Sitzung zu einer neuen Topologie wechselt oder die aktuelle Topologie löscht, wird das Knoten Objekt wie folgt heruntergefahren:
<ul>
<li>Ausgabe Knoten: die Sitzung ruft <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>imfmediasink:: Shutdown</strong></a> für die Medien Senke auf.</li>
<li>Transformations Knoten: die Sitzung ruft <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>imfshutdown:: Shutdown</strong></a> für die MFT auf.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Der Standardwert ist " **true**".

Wenn Ihre Anwendung mehrere Topologien in die Warteschlange stellt, empfiehlt es sich, dieses Attribut auf " **false**" festzulegen. Andernfalls werden Objekte in der Topologie möglicherweise nicht ordnungsgemäß heruntergefahren.

Dieses Attribut gilt nicht, wenn die Anwendung die Medien Sitzung durch Aufrufen von [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)herunterfährt. Wenn die Medien Sitzung heruntergefahren wird, werden die Medien senken und asynchrone MFTs in der aktuellen Topologie immer heruntergefahren.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




