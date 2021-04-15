---
title: IDWriteTextAnalyzer2-Schnittstelle
description: Analysiert verschiedene Texteigenschaften für die Verarbeitung komplexer Skripts.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- IDWriteTextAnalyzer2 Interface Direct Write
- IDWriteTextAnalyzer2 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518107"
---
# <a name="idwritetextanalyzer2-interface"></a>IDWriteTextAnalyzer2-Schnittstelle

Analysiert verschiedene Texteigenschaften für die Verarbeitung komplexer Skripts.

## <a name="members"></a>Member

Die **IDWriteTextAnalyzer2** -Schnittstelle erbt von [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1). **IDWriteTextAnalyzer2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteTextAnalyzer2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Checktypographicfeature**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Überprüft, ob ein typografisches Feature für ein Symbol oder einen Satz von Symbolen verfügbar ist.<br/> |
| [**Getglyphorientationtransform**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Gibt eine 2x3-Transformationsmatrix für den jeweiligen Winkel zum Zeichnen der Symbol Führung zurück.<br/> |
| [**Gettypographicfeatures**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Gibt eine vollständige Liste der OpenType-Funktionen zurück, die für ein Skript oder eine Schriftart verfügbar sind.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

