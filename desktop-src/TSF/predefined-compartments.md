---
title: Vordefinierte Depots (ctffunc. h)
description: Die folgenden Werte identifizieren Depots, die durch das Text Dienste-Framework implementiert werden.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Vordefinierte Depots-Text Dienst-Framework
topic_type:
- apiref
api_name:
- Predefined Compartments
api_location:
- Ctffunc.h
- Mstctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc684c4aee55c3c2e1807458ee261ad55156e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105392"
---
# <a name="predefined-compartments"></a>Vordefinierte Depots

Die folgenden Werte identifizieren Depots, die durch das Text Dienste-Framework implementiert werden.

Die folgenden Depot Bezeichner sind in ctffunc. idl und ctffunc. h definiert.



| Flag                                     | Wert  | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ \_ -Depot SAPI \_ -Audiodatei           | VT \_ I4 | Ein **DWORD** , das 0 (null) ist, wenn die Spracheingabe-API (SAPI) Off oder nicht 0 ist, wenn die SAPI-Audiodatei aktiviert ist. Dieses Depot ist spezifisch für ein Thread-Manager-Objekt.                                                                                                                               |
| Spracheingabe \_ - \_ \_ cfgmenu für GUID-Depot       | VT \_ I4 | Ein **DWORD** , das 0 (null) ist, wenn das sprach Konfigurationsmenü nicht verfügbar ist Dieses Depot ist spezifisch für ein Thread-Manager-Objekt.                                                                                               |
| Sprachausgabe für GUID-Depot \_ \_ \_ | VT \_ I4 | Ein **DWORD** -Wert, der 0 (null) oder eine Kombination aus einer oder mehreren der [**\_ \_ aktivierten TF-diktierung**](speech-recognition-constants.md), **tf- \_ Befehlszeilen \_ Aktivierung**, **tf- \_ Diktat \_** oder TF-Befehle **\_ \_ für** Werte enthält. Dieses Depot ist spezifisch für ein Thread-Manager-Objekt. |
| Status der \_ \_ \_ Benutzeroberfläche \_ der GUID-Depot Sprache    | VT \_ I4 | Ein **DWORD** -Wert, der 0 (null) oder eine Kombination aus einem oder mehreren der [**tf \_ Show \_**](speech-recognition-constants.md) Sprechblasen-oder TF-Sprechblasen Werte enthält. **\_ \_** Dabei handelt es sich um ein globales Depot.                                                                                   |



 

Die folgenden Depot Bezeichner sind in msctf definiert. IDL und msctf. H.



| Flag                                                    | Wert  | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID-Depot \_ \_ emptycontext                         | VT \_ I4 | Ein **DWORD** , das ungleich 0 (null) ist, wenn der Kontext leer ist, andernfalls NULL. Dieses Depot ist spezifisch für ein Kontext Objekt.                                                                                                                                      |
| Handschrift des GUID-Depots \_ \_ \_ openclose               | VT \_ I4 | Ein **DWORD** , das ungleich NULL ist, wenn die Handschrifterkennung geöffnet ist, oder 0 (null), wenn die Handschrifterkennung geschlossen ist Dieses Depot ist spezifisch für ein Thread-Manager-Objekt.                                                                                 |
| GUID-Depot- \_ \_ Tastatur \_ deaktiviert                   | VT \_ I4 | Ein **DWORD** , das ungleich 0 (null) ist, wenn die Tastatur deaktiviert ist, andernfalls NULL. Dieses Depot ist spezifisch für ein Kontext Objekt.                                                                                                                                  |
| GUID-Depot \_ \_ Tastatur- \_ InputMode- \_ Konvertierung      | VT \_ I4 | Ein **DWORD** -Wert, der die richtige Kombination von [**tf- \_ konform \_**](flags-for-conversion-mode.md) ist. Dieses Depot ist spezifisch für ein Thread-Manager-Objekt.                                                                                      |
| GUID-Depot \_ \_ Tastatur \_ InputMode- \_ Satz        | VT \_ I4 | Ein **DWORD** -Wert von [**tf \_ sentencemode \_**](flags-for-conversion-mode.md). Dieses Depot ist spezifisch für ein Thread-Manager-Objekt.                                                                                                                        |
| GUID-Depot, \_ \_ Tastatur \_ openclose                  | VT \_ I4 | Ein **DWORD** , das ungleich NULL ist, wenn die Tastatur geöffnet ist, oder 0 (null), wenn die Tastatur geschlossen ist. Dieses Depot ist spezifisch für ein Thread-Manager-Objekt.                                                                                                               |
| GUID-Depot \_ \_ persistmenuaktivierte                   | VT \_ I4 | Ein **DWORD** , das ungleich NULL ist, damit der sprach Text Dienst das Menü Element " **Sprach Daten speichern** " oder "0" (null) aktivieren kann, um es zu deaktivieren Dieses Depot ist spezifisch für ein Dokument-Manager-Objekt.                                                                   |
| Sprache des GUID-Depots \_ \_ \_ deaktiviert                     | VT \_ I4 | Ein **DWORD** , das 0 (null) oder eine Kombination aus einem oder mehreren der TF-Deaktivierungs [**\_ \_ Sprache**](speech-recognition-constants.md), **tf \_ deaktiviert \_** oder **tf deaktiviert \_ \_ Befehls** Werte enthält. Dieses Depot ist spezifisch für ein Thread-Manager-Objekt. |
| Stimme des GUID-Depots \_ \_ \_ openclose                    | VT \_ I4 | Ein **DWORD** , das ungleich 0 (null) ist, wenn die Spracheingabe aktiv ist, oder 0 (null), wenn die Sprache Dabei handelt es sich um ein globales Depot.                                                                                                                                      |
| GUID \_ Depot \_ tipuistatus                          | VT \_ I4 | Derzeit nicht verwendet.                                                                                                                                                                                                                                           |
| Erweiterung des GUID-Depots \_ \_ transitor                  | VT \_ I4 | Der **DWORD** -Wert [**tf \_ transitor Extension \_ None**](values-for-guid-compartment-transitoryextension.md), **tf \_ transitor Extension \_ Floating** oder **tf \_ transitor Extension \_ atselection**. Dieses Depot ist spezifisch für ein Dokument-Manager-Objekt.  |
| "GUID Depot \_ \_ transitor Extension" \_ documentmanager | VT \_ I4 | Ein IUnknown-Wert für die [**ITF documentmgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) -Schnittstelle, die das vorübergehendes-Dokument dieses Dokument-Managers bezeichnet. Dieses Depot ist spezifisch für ein Dokument-Manager-Objekt.                                                         |
| übergeordnetes Element des GUID-Depots \_ \_ transitor \_          | VT \_ I4 | Ein IUnknown-Wert für die [**ITF documentmgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) -Schnittstelle, die den übergeordneten Dokument-Manager dieses vorübergehendes-Dokuments bezeichnet. Dieses Depot ist spezifisch für ein Dokument-Manager-Objekt.                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                                                                                          |
| Header<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Mstctf. h</dt> </dl>     |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Mstctf. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sprach Erkennungs Konstanten**](speech-recognition-constants.md)
</dt> </dl>

 

 





