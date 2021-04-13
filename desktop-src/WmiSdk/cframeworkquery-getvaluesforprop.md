---
description: Die getvaluesforprop-Methode gibt alle Werte für eine bestimmte Eigenschaft zurück, die von dieser Eigenschaft generiert werden, so wie Sie in der Abfrage angezeigt wird.
audience: developer
ms.assetid: b5ed4b48-f622-4a55-897d-d800ada0270f
ms.tgt_platform: multiple
title: 'Cframeworkquery:: getvaluesforprop-Methode (frquery. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b5fd9dbc22289843141c517203809045abbf05a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217135"
---
# <a name="cframeworkquerygetvaluesforprop-methods"></a>Cframeworkquery:: getvaluesforprop-Methoden

\[Die [**cframeworkquery**](/windows/win32/api/frquery/nl-frquery-cframeworkquery) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die **getvaluesforprop** -Methode gibt alle Werte für eine bestimmte Eigenschaft zurück, die von dieser Eigenschaft generiert werden, so wie Sie in der Abfrage angezeigt wird.

Beispielsweise gibt ein Aufrufen von **getvaluesforprop**(L "Name", SA) das Array *sa* zurück, das alle Werte von "Name" enthält, die erfordern, dass Instanzen zurückgesendet werden, um die Abfrage zu erfüllen. Wenn *sa* {"a", "b"} enthält, werden alle Instanzen, in denen "Name = a" steht, sowie alle Instanzen, in denen "Name = b" zurückgesendet werden muss, zurückgesendet, um die Abfrage vollständig zu erfüllen.

Wenn die Einschränkungen für "Name" nicht ausreichend eingeschränkt sind, wird ein leeres *sa* -Array zurückgegeben.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                             | BESCHREIBUNG                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Getvaluesforprop (chstringarray&, LPCWSTR)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_))                      | Gibt alle Werte für eine bestimmte Eigenschaft zurück, die von dieser Eigenschaft generiert werden, so wie Sie in der Abfrage angezeigt wird.<br/> |
| [**Getvaluesforprop (LPCWSTR, Std:: Vector &lt; \_ BSTR \_ t &gt;&)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_std-vector__bstr_t__)) | Gibt alle Werte für eine bestimmte Eigenschaft zurück, die von dieser Eigenschaft generiert werden, so wie Sie in der Abfrage angezeigt wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Frquery. h (Include-Datei "f")</dt> </dl>                                                     |
| Bibliothek<br/>                  | <dl> <dt>Framedyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
