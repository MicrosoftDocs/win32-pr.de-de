---
description: Eine überladene Methode, die den Speicher frei gibt, der den Pfad enthält.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: CObjectPathParser::Free-Methoden (ObjPath.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0e7e5e366d96d4c8b5c6d82f177a480114c5d6356759c8db46389c809aea7137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819806"
---
# <a name="cobjectpathparserfree-methods"></a>CObjectPathParser::Free-Methoden

\[Die [**CObjectPathParser-Klasse**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) ist Teil des WMI-Anbieterframework, das jetzt als endgültig betrachtet wird, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken betreffen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Eine überladene Methode, die den Speicher frei gibt, der den Pfad enthält.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                     | BESCHREIBUNG                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))                     | Gibt den Arbeitsspeicher frei, der den nicht verarbeiteten Pfad enthält.<br/>                      |
| [**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath)) | Gibt den Arbeitsspeicher frei, der die Struktur enthält, die über den analysierten Pfad verfügt.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ObjPath.h (objPath.h enthalten)</dt> </dl>                                                      |
| Bibliothek<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

�

�
