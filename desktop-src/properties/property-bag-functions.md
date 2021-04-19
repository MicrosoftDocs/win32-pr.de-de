---
description: In diesem Abschnitt wird eine Reihe von Windows-Hilfsfunktionen beschrieben, die mit IPropertyBag-Objekten verwendet werden.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Eigenschaften Behälter Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c86a2e3ce61805702641f893d51f5c4aa26b0ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349905"
---
# <a name="property-bag-functions"></a>Eigenschaften Behälter Funktionen

In diesem Abschnitt wird eine Reihe von Windows-Hilfsfunktionen beschrieben, die mit [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) -Objekten verwendet werden.



| Thema                                                                       | Inhalte                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Pspropertybag \_ Löschen**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Löscht eine Eigenschaft aus einem Eigenschaften Behälter.<br/>                                                                           |
| [**Pspropertybag (Read \_ bool)**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Liest den **booleschen** Datenwert einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                    |
| [**Pspropertybag- \_ leserbstr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Liest einen **BSTR** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                    |
| [**Pspropertybag- \_ /DWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Liest einen **DWORD** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                     |
| [**Pspropertybag- \_ leserguid**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Liest den GUID-Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                      |
| [**Pspropertybag-Read- \_ int**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Liest einen **int** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                    |
| [**Pspropertybag, \_ lesbar**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Liest einen **Long** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                    |
| [**Pspropertybag (Read \_ pointl)**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Ruft die in einer [**pointl**](/previous-versions//dd162807(v=vs.85)) -Struktur eines angegebenen Eigenschaften Behälters gespeicherten Eigenschaften Koordinaten ab.<br/>    |
| [**Pspropertybag- \_ Punkte**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Ruft die in einer [**Punkt**](/previous-versions//dd162808(v=vs.85)) Struktur eines angegebenen Eigenschaften Behälters gespeicherten Eigenschaften Koordinaten ab.<br/>    |
| [**Pspropertybag, Read \_ PropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Liest den Eigenschafts Schlüssel einer Eigenschaft in einem angegebenen Eigenschaften Behälter.<br/>                                                 |
| [**Pspropertybag- \_ leserrectl**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Ruft die Koordinaten eines Rechtecks ab, das in einer Eigenschaft gespeichert ist, die in einem angegebenen Eigenschaften Behälter enthalten ist.<br/>              |
| [**Pspropertybag-Read \_ Short**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Liest den **kurzen** Datenwert einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                   |
| [**Pspropertybag- \_ Lesung**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Liest den **Zeichen** folgen Daten Wert einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                                  |
| [**Pspropertybag-Read- \_ zuzuweisung**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Liest einen **Zeichen** folgen Daten Wert aus einer Eigenschaft in einem Eigenschaften Behälter und ordnet den Speicher für die gelesene Zeichenfolge zu.<br/> |
| [**Pspropertybag-Daten \_ Strom**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Liest den Datenstrom, der in einer angegebenen Eigenschaft gespeichert ist, die in einem angegebenen Eigenschaften Behälter enthalten ist.<br/>                           |
| [**Pspropertybag- \_ lestype**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Liest den Typ des Daten Werts einer Eigenschaft, die in einem Eigenschaften Behälter gespeichert ist.<br/>                                      |
| [**Pspropertybag- \_ Aufgabe**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Liest einen **ULONGLONG** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter.<br/>                                               |
| [**Pspropertybag- \_ lesunknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Liest eine angegebene Eigenschaft eines unbekannten Daten Werts in einem Eigenschaften Behälter.<br/>                                                |
| [**Pspropertybag- \_ beschreitebool**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Legt den **booleschen** Datenwert einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                     |
| [**Pspropertybag- \_ beschreitebstr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Legt einen **BSTR** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                     |
| [**Pspropertybag- \_ beschreitedword**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Legt einen **DWORD** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                      |
| [**Pspropertybag- \_ Schreib-GUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Legt den GUID-Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                       |
| [**Pspropertybag- \_ Schreib Wort**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Legt einen **int** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                     |
| [**Pspropertybag \_ schreibong**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Legt einen **Long** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                     |
| [**Pspropertybag- \_ Beschreib tepointl**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Speichert die in einer [**pointl**](/previous-versions//dd162807(v=vs.85)) -Struktur eines angegebenen Eigenschaften Behälters gespeicherten Eigenschaften Koordinaten.<br/>       |
| [**Pspropertybag- \_ Schreib Punkte**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Speichert die Eigenschaften Koordinaten, die in einer [**Punkt**](/previous-versions//dd162808(v=vs.85)) Struktur eines angegebenen Eigenschaften Behälters gespeichert sind.<br/>       |
| [**Pspropertybag- \_ Beschreib tepropertykey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Legt den Eigenschafts Schlüssel einer Eigenschaft in einem angegebenen Eigenschaften Behälter fest.<br/>                                                  |
| [**Pspropertybag- \_ beschreiterectl**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Speichert die Koordinaten eines Rechtecks, das in einer Eigenschaft gespeichert ist, die in einem angegebenen Eigenschaften Behälter enthalten ist.<br/>                 |
| [**Pspropertybag- \_ schreibgeschützte**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Legt den **kurzen** Datenwert einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                    |
| [**Pspropertybag- \_ Schreib testr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Legt den **Zeichen** folgen Datenwert einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                   |
| [**Pspropertybag- \_ Schreibvorgang**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Legt den Datenstrom fest, der in einer angegebenen Eigenschaft gespeichert ist, die in einem angegebenen Eigenschaften Behälter enthalten ist.<br/>                            |
| [**Pspropertybag- \_ Schreibvorgang**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Legt einen **ULONGLONG** -Datenwert aus einer Eigenschaft in einem Eigenschaften Behälter fest.<br/>                                                |
| [**Pspropertybag \_ beschreibunknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Legt eine angegebene Eigenschaft eines unbekannten Daten Werts in einem Eigenschaften Behälter fest.<br/>                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PROPVARIANT und VARIANT (Funktionen)](./functions-propvarutil.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> </dl>

 

 
