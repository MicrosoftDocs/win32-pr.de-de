---
description: Schließt alle erforderlichen Vorgänge für den metadatenpuffer ab und gibt das angegebene ispatialaudiometadataitems-Objekt frei.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Ispatialaudiometadatawriter:: Close-Methode'
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
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127312"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>Ispatialaudiometadatawriter:: Close-Methode

Schließt alle erforderlichen Vorgänge für den metadatenpuffer ab und gibt das angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) -Objekt frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, enthalten mögliche Rückgabecodes die in der folgenden Tabelle aufgeführten Werte, sind jedoch nicht darauf beschränkt.



| Rückgabecode                                                                                                                     | Beschreibung                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**sptlaud \_ MD \_ CLNT \_ E \_ keine \_ Elemente \_ geöffnet**</dt> </dl>            | Das angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) wurde nicht mit einem geöffneten [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open)-Befehl geöffnet.<br/> |
| <dl> <dt>**sptlaud \_ MD \_ CLNT \_ E \_ keine \_ Elemente \_ geschrieben**</dt> </dl>         | Es wurden keine Metadatenelemente in das angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)geschrieben.<br/>                                              |
| <dl> <dt>**das Element "sptlaud \_ MD \_ CLNT \_ E" \_ \_ muss \_ über \_ Befehle verfügen.**</dt> </dl> | Es wurden keine metadatenbefehle in die angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)geschrieben.<br/>                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ispatialaudiometadatawriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




