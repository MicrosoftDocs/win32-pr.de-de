---
description: Definiert standardmäßige, spezifische und generische Rechte. Diese Rechte werden in Zugriffs Steuerungs Einträgen (Access Control Entries, ACEs) verwendet und sind das primäre Mittel zum Angeben des angeforderten oder gewährten Zugriffs auf ein Objekt.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131449"
---
# <a name="access_mask"></a>Zugriffs \_ Maske

Der **Access \_ Mask** -Datentyp ist ein **DWORD** -Wert, der Standard-, spezifische und generische Rechte definiert. Diese Rechte werden in [*Zugriffs Steuerungs Einträgen (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs) verwendet und sind das primäre Mittel zum Angeben des angeforderten oder gewährten Zugriffs auf ein Objekt.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Bemerkungen

Die Bits in diesem Wert werden wie folgt zugeordnet.



| Bits             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Bestimmte Rechte. Enthält die für den Objekttyp spezifische Zugriffs Maske, die der Maske zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Standard Rechte. Enthält die Standard Zugriffsrechte des-Objekts.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Zugreifen auf die Systemsicherheit (**Zugriffs \_ System \_ Sicherheit**). Es wird verwendet, um den Zugriff auf eine SACL ( [*System Access Control List*](/windows/desktop/SecGloss/s-gly) ) anzugeben. Diese Art von Zugriff erfordert, dass der Aufrufprozess über die Berechtigung **SE \_ Security \_ Name** (Überwachungs-und Sicherheitsprotokoll verwalten) verfügt. Wenn dieses Flag in der Zugriffs Maske eines Überwachungs Zugriffs-ACE (erfolgreicher oder nicht erfolgreicher Zugriff) festgelegt ist, wird der Zugriff auf die SACL überwacht.<br/> |
| 25<br/>    | Maximal zulässig (**maximal \_ zulässig**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Generisch,**alle \_ (generisch**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Generisch ausführen (**generisches \_ Ausführen**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Generischer Schreibvorgang (**generischer \_ Schreib** Vorgang).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Generischer Lesevorgang (**generischer \_ Lese** Vorgang).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

Die Standardrechte Bits (16 bis 23) enthalten die Standard Zugriffsrechte des Objekts und können eine Kombination der folgenden vordefinierten Flags sein.



| bit           | Flag                         | Bedeutung                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Löschen Sie den Zugriff.<br/>                                                                                                                                                                                                                |
| 17<br/> | **Lese \_ Steuerelement**<br/> | Lesezugriff auf den Besitzer, die Gruppe und die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) der Sicherheits Beschreibung.<br/> |
| 18<br/> | **\_DAC schreiben**<br/>    | Schreibzugriff auf die DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **\_Besitzer schreiben**<br/>  | Schreibzugriff auf Besitzer.<br/>                                                                                                                                                                                                        |
| 20<br/> | **SYNCHRONIZE**<br/>   | Synchronisieren Sie den Zugriff.<br/>                                                                                                                                                                                                           |



 

Die folgenden Konstanten, die in Winnt. h definiert sind, stellen die spezifischen und standardmäßigen Zugriffsrechte dar.


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zugriffssteuerung](access-control.md)
</dt> <dt>

[Grundlegende Access Control Strukturen](authorization-structures.md)
</dt> <dt>

[Zugriffsrechte und Zugriffs Masken](access-rights-and-access-masks.md)
</dt> <dt>

[**generische \_ Zuordnung**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

