---
description: Stellt Methoden zum Bereitstellen von Browsereinstellungen bereit. Die iitempreviewerext-Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Iitempreviewerext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958782"
---
# <a name="iitempreviewerext-interface"></a>Iitempreviewerext-Schnittstelle

Stellt Methoden zum Bereitstellen von Browsereinstellungen bereit. Die **iitempreviewerext** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

## <a name="members"></a>Member

Die **iitempreviewerext** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iitempreviewerext** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iitempreviewerext** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Getlinkedcontent**](-search-iitempreviewerext-getlinkedcontent.md)               | Ermöglicht der Erweiterung den umfangreichen Inhalt für eine Eigenschaft. <br/>                            |
| [**Getrelatedpart**](-search-iitempreviewerext-getrelatedpart.md)                   | Ruft einen zugehörigen Textteil zum Einbetten in den MHTML-Ausgabedatenstrom ab.<br/>              |
| [**Processtransformcommand**](-search-iitempreviewerext-processtransformcommand.md) | Ermöglicht die Verarbeitung eines Transformations Befehls, der in einer Vorschau Vorlage gefunden wurde.<br/> |
| [**Vorschlags Suchrichtlinie**](-search-iitempreviewerext-suggestbrowserpolicy.md)       | Schlägt die Sicherheitsrichtlinie vor, die auf den Browser angewendet werden soll.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Die **iitempreviewerext** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **iitempreviewerext** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



 

 
