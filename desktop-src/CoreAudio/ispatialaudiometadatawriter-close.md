---
description: Schließt alle erforderlichen Vorgänge für den Metadatenpuffer ab und gibt das angegebene ISpatialAudioMetadataItems-Objekt frei.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: ISpatialAudioMetadataWriter::Close-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 4b29efb38cf11ba718a631f676323eb3db93aab042c70691dfb89ce957266e86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875420"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>ISpatialAudioMetadataWriter::Close-Methode

Schließt alle erforderlichen Vorgänge für den Metadatenpuffer ab und gibt das angegebene [**ISpatialAudioMetadataItems-Objekt**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, enthalten mögliche Rückgabecodes die in der folgenden Tabelle aufgeführten Werte, sind aber nicht darauf beschränkt.



| Rückgabecode                                                                                                                     | Beschreibung                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ NO \_ ITEMS \_ OPEN**</dt> </dl>            | Das angegebene [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) wurde nicht mit einem Aufruf von [**Öffnen**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open)geöffnet.<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E KEINE \_ \_ \_ GESCHRIEBENEN ELEMENTE**</dt> </dl>         | Es wurden keine Metadatenelemente in das angegebene [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)geschrieben.<br/>                                              |
| <dl> <dt>**SPTLAUD MD CLNT E ITEM MUST HAVE COMMANDS (SPTLAUD \_ MD \_ CLNT \_ \_ \_ E-ELEMENT MUSS \_ BEFEHLE \_ AUFWEISEN)**</dt> </dl> | Es wurden keine Metadatenbefehle in das angegebene [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)geschrieben.<br/>                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




