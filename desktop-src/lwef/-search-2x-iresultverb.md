---
title: Iresultverb-Schnittstelle (wdssharedidl. h)
description: Macht Verb Eigenschaften verfügbar.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Iresultverb Interface Legacy Windows-Umgebungs Features
- Iresultverb Interface Legacy Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339991"
---
# <a name="iresultverb-interface"></a>Iresultverb-Schnittstelle

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Macht Verb Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iresultverb** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iresultverb** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **iresultverb** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresultverb-displayname.md)<br/> | Schreibgeschützt<br/>  | Diese Eigenschaft gibt einen Zeiger auf den lokalisierten anzeigen Amen für das Verb zurück. <br/>                           |
| [**Doit**](-search-2x-iresultverb-doit.md)<br/>               | Lesegeschützt<br/> | Führt das Verb aus. <br/>                                                                                    |
| [**Aktiviert**](-search-2x-iresultverb-enabled.md)<br/>         | Schreibgeschützt<br/>  | Diese Eigenschaft gibt true zurück, wenn das Verb aktiviert ist. <br/>                                                    |
| [**HelpText**](-search-2x-iresultverb-helptext.md)<br/>       | Schreibgeschützt<br/>  | Diese Eigenschaft gibt einen Zeiger auf die lokalisierte Hilfe Zeichenfolge für das Verb zurück. <br/>                            |
| [**Symbol**](-search-2x-iresultverb-icon.md)<br/>               | Schreibgeschützt<br/>  | Diese Eigenschaft gibt einen Zeiger auf das Handle des optionalen Symbols zurück, das dem Verb zugeordnet ist. <br/>              |
| [**Name**](-search-2x-iresultverb-name.md)<br/>               | Schreibgeschützt<br/>  | Diese Eigenschaft gibt einen Zeiger auf den Kontonamen für das Verb zurück, z. b. "Drucken", "Öffnen" usw. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methoden machen Eigenschaften und Aktionen verfügbar, die auf Verben anwendbar sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

