---
title: Vordefinierte Eigenschaften (msctf. h)
description: Die folgenden Werte identifizieren TSF-definierte Eigenschaften. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.
ms.assetid: d88f2eba-4c98-4b32-96e1-cd019fe0f7ad
keywords:
- Vordefinierte Eigenschaften Text Dienst-Framework
topic_type:
- apiref
api_name:
- Predefined Properties
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807d1be5d1cc025971ad294fac825b89a4a0a519
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346109"
---
# <a name="predefined-properties"></a>Vordefinierte Eigenschaften

Die folgenden Werte identifizieren TSF-definierte Eigenschaften. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.

## <a name="properties"></a>Eigenschaften



| Eigenschaft                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID- \_ Prop- \_ Attribut**       | Enthält einen [**tfguidatom**](tfguidatom.md) -Wert, der die **GUID** des Anzeige Attributs darstellt. [**Itfcategorymgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) wird verwendet, um diesen Wert in eine **GUID** zu konvertieren. Weitere Informationen finden Sie unter [Verwenden von Anzeige Attributen](using-display-attributes.md).                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID- \_ Prop \_ textowner**       | Enthält einen [**tfguidatom**](tfguidatom.md) -Wert, der den Klassen Bezeichner ( **CLSID** ) des Text dienstaners darstellt, der den Text besitzt. [**Itfcategorymgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) wird verwendet, um diesen Wert in eine **CLSID** zu konvertieren.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **GUID- \_ Prop- \_ LangID**          | Enthält einen **DWORD** -Wert, der den sprach Bezeichner ( **LangID** ) des Texts im unteren Wort enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Lesen von GUID- \_ Prop \_**         | Enthält den phonetischen Lesetext für den von der-Eigenschaft behandelten Text. Dies kann sich vom eigentlichen Text unterscheiden. Windows Store-Apps unterstützen diese Eigenschaft nicht.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **GUID- \_ Prop- \_ Komposition**       | Enthält einen booleschen Wert, der ungleich 0 (null) ist, wenn der Text Teil einer Komposition ist, andernfalls NULL. Wenn diese Eigenschaft "VT \_ empty" ist, kann davon ausgegangen werden, dass der Text nicht Teil einer Komposition ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **GUID- \_ Prop \_ modebias**        | Enthält einen [**tfguidatom**](tfguidatom.md) -Wert, der den Typ der unterstützten modusbias darstellt. [**Itfcategorymgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) wird verwendet, um diesen Wert in eine **GUID** zu konvertieren. Dies kann einer der Modus- [**biaswerte**](mode-bias-values.md)sein.                                                                                                                                                                                                                                                                                                                                                                                                  |
| **GUID- \_ Prop \_ Liebe meine lifeattice**       | Enthält einen Zeiger auf ein [**itflmlattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice) -Objekt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID- \_ Prop- \_ TKB- \_ Alternativen** | **Beginnend mit Windows 8:** Enthält einen von der Touchscreen-Tastatur festgelegten **DWORD** -Wert. Diese Eigenschaft kann von TSF-fähigen Bearbeitungs Steuerelementen und Apps verwendet werden, um die Art des Texts im Textbereich zu identifizieren, der von der-Eigenschaft abgedeckt wird, z. b. wenn der Text im Bereich aus dem Einfügen eines Text Vorschlags oder einer AutoKorrektur resultiert. <br/> Die Art des Texts im Textbereich, der von der-Eigenschaft abgedeckt wird, erstreckt sich auch auf den Typ der Alternativen, die von der [**itffnreconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) -Schnittstelle für diesen Textbereich im Dokument zurückgegeben werden.<br/> In den folgenden Anmerkungen finden Sie die möglichen Werte dieser Eigenschaft.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **GUID-Eigenschaft " \_ \_ TKB- \_ Alternativen** " kann einen der folgenden Werte aufweisen.



| Name                                     | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TKB \_ wechselt \_ Standard                | 0x00000001 | Gibt an, dass die Berührungs Tastatur eine Liste möglicher alternativer Wörter für den Text im von der-Eigenschaft abgedeckten Bereich generiert hat und weder der Textbereich noch die Alternativen eine automatische Korrektur oder ein Textvorschlag sind.                                                                                                                                                                                                              |
| TKB- \_ Alternativen \_ für die \_ Automatische Korrektur     | 0x00000002 | Gibt an, dass die Berührungs Tastatur ein alternatives Wort generiert hat, das automatisch den Text im Textbereich ersetzen soll, der durch die-Eigenschaft abgedeckt wird.<br/> Die Tastenkombination wendet die automatische Korrektur nicht an, ohne dass Sie vom Bearbeitungs Steuerelement oder der APP dazu aufgefordert wird. Die erneuten Konvertierung gelöscht-Schnittstelle ([**itffnreconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)) sollte zum Anwenden der Korrektur auf den Text im Dokument verwendet werden.<br/> |
| TKB- \_ Alternativen \_ für \_ Vorhersage         | 0x00000003 | Gibt an, dass der von der-Eigenschaft abgedeckte Textbereich ein Textvorschlag ist, der von der Touchscreen-Tastatur generiert und vom Benutzer in das Dokument eingefügt wurde.<br/> Weitere Alternative Vorhersagen können auch als Eigenschaft im Dokument gespeichert werden.<br/>                                                                                                                                                                     |
| TKB- \_ Alternative \_ Automatische Korrektur \_ wird angewendet | 0x00000004 | Gibt an, dass der von der-Eigenschaft abgedeckte Textbereich eine von der Touchscreen-Tastatur bereitgestellte und über die [**itffnreconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) -Schnittstelle angewendete automatische Korrektur ist.<br/> Dieser Wert kann von Edit-Steuerelementen oder-Apps verwendet werden, wobei TKB \_ \_ für \_ die automatische Korrektur verwendet werden, um die wiederholte Anwendung einer AutoKorrektur zu verhindern.<br/>                                                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tfguidatom**](tfguidatom.md)
</dt> <dt>

[**ITF categorymgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[Verwenden von Anzeige Attributen](using-display-attributes.md)
</dt> <dt>

[**Modus-biaswerte**](mode-bias-values.md)
</dt> <dt>

[**Itflmlattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)
</dt> </dl>

 

 





