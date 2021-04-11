---
description: Wird zum Anfügen an eine bestimmte Smartcard oder einen Leser verwendet, um andere optionale Schnittstellen zum Ausführen spezifischer Smartcardfunktionen zu erstellen, eine bestimmte Smartcard für die exklusive Verwendung zu sperren und den Status einer Smartcard oder eines Readers zu erhalten.
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: Iscardmanage-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: cce31ea21701c098b09a0bd96360afb374a9bccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217759"
---
# <a name="iscardmanage-interface"></a>Iscardmanage-Schnittstelle

\[Die **iscardmanage** -Schnittstelle ist nicht mehr für die Verwendung ab Windows Server 2008, Windows Vista und Windows Server 2003 mit Service Pack 1 (SP1) und höher verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die folgende Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard*](../secgloss/s-gly.md) - [*Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann.

Die **iscardmanage** -Schnittstelle muss bereitgestellt werden. Sie wird zum Anfügen an eine bestimmte [*Smartcard*](../secgloss/s-gly.md) oder einen [*Leser*](../secgloss/r-gly.md)verwendet, um andere optionale Schnittstellen zum Ausführen bestimmter Smartcardfunktionen zu erstellen, eine bestimmte Smartcard für die exklusive Verwendung zu sperren und den Status einer Smartcard oder eines Readers zu erhalten. Als Gruppe können diese Dienste für die Verwaltung eines klar definierten Kontexts verantwortlich sein, in dem eine Anwendung mit einer [*Smartcard*](../secgloss/s-gly.md) oder einem [*Reader*](../secgloss/r-gly.md)kommunizieren kann.

Im folgenden finden Sie eine typische Verwendung der **iscardmanage** -Schnittstelle.

**So stellen Sie eine Verbindung mit einer Smartcard her**

1.  Erstellen Sie die **iscardmanage** -Schnittstelle, die der Karte zugeordnet ist.
2.  Stellen Sie eine Verbindung zu einer Smartcard her, indem Sie Sie an einen bestimmten Smartcardleser ([**attachbyifd**](iscardmanage-attachbyifd.md)) anfügen, oder indem Sie ein zuvor erworbenes handle ([**attachbyhandle**](iscardmanage-attachbyhandle.md)) verwenden.
3.  Erstellen Sie andere Schnittstellen zum Durchführen von smartcardvorgängen ("[**kreatecardauth**](iscardmanage-createcardauth.md)", "up [**File Access**](iscardmanage-createfileaccess.md)", " [**kreatechverification**](iscardmanage-createchverification.md)" oder " [**kreateinterface**](iscardmanage-createinterface.md)").
4.  Geben Sie die Karte frei ([**trennen**](iscardmanage-detach.md)).
5.  Geben Sie die **iscardmanage** -Schnittstelle und andere nach Bedarf frei.

## <a name="members"></a>Member

Die **iscardmanage** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscardmanage** verfügt auch über die folgenden Typen von Mitgliedern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscardmanage** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attachbyhandle**](iscardmanage-attachbyhandle.md)             | Ermöglicht es einer Anwendung, mithilfe eines Handles, das von der Smartcard- [*Ressourcen-Manager*](../secgloss/r-gly.md)zurückgegeben wird, eine Kommunikations Verknüpfung zu einer Smartcard zu erstellen.<br/>                                              |
| [**Attachbyifd**](iscardmanage-attachbyifd.md)                   | Ermöglicht es einer Anwendung, die Einrichtung eines Kontexts für einen bestimmten Reader anzufordern, auf den mit einem anzeigen Amen verwiesen wird.<br/>                                                                                                                                               |
| [**"Kreatecardauth"**](iscardmanage-createcardauth.md)             | Ermöglicht die Erstellung einer [**iscardauth**](iscardauth.md) -Schnittstelle.<br/>                                                                                                                                                                                            |
| [**"Kreatechverification"**](iscardmanage-createchverification.md) | Ermöglicht die Erstellung einer [**iscardverify**](iscardverify.md) -Schnittstelle.<br/>                                                                                                                                                                                        |
| [**"Kreatefileaccess"**](iscardmanage-createfileaccess.md)         | Ermöglicht die Erstellung einer [**iscardfileaccess**](iscardfileaccess.md) -Schnittstelle.<br/>                                                                                                                                                                                |
| [**"Kreatabterface"**](iscardmanage-createinterface.md)           | Ermöglicht das Erstellen einer Schnittstelle.<br/>                                                                                                                                                                                                                            |
| [**Trennen**](iscardmanage-detach.md)                             | Gibt die Anlage auf einer bestimmten Smartcard oder einem Leser frei, der von [**attachbyhandle**](iscardmanage-attachbyhandle.md) bzw. [**attachbyifd**](iscardmanage-attachbyifd.md) zugeordnet wird.<br/>                                                                |
| [**Verbindung wiederherstellen**](iscardmanage-reconnect.md)                       | Ermöglicht es einer Anwendung, erneut eine Verbindung mit einer Smartcard oder einem Reader herzustellen, ohne eine Trennung [**, gefolgt von**](iscardmanage-detach.md) [**attachbyhandle**](iscardmanage-attachbyhandle.md) oder [**attachbyifd**](iscardmanage-attachbyifd.md) , ausgeben zu müssen.<br/> |
| [**Scardlock**](iscardmanage-scardlock.md)                       | Sperrt eine verbundene Smartcard oder einen verbundenen Reader für die exklusive Verwendung.<br/>                                                                                                                                                                                                       |
| [**Scardunlock**](iscardmanage-scardunlock.md)                   | Gibt die exklusive Verwendung der verbundenen Smartcard oder des Readers frei.<br/>                                                                                                                                                                                                   |
| [**Status**](iscardmanage-status.md)                             | Ermöglicht es einer Anwendung, den aktuellen Status der Smartcard oder des Readers zu erhalten.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

 
