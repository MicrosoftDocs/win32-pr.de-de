---
description: Definiert Standard-, spezifische und generische Rechte. Diese Rechte werden in Zugriffssteuerungseinträgen (Access Control Entries, ACEs) verwendet und sind die primäre Möglichkeit, den angeforderten oder gewährten Zugriff auf ein Objekt anzugeben.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13378b44d17bedd818efd5fc84310b304a2f683a3331237e8cca208be8de810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785467"
---
# <a name="access_mask"></a>ACCESS \_ MASK

Der **ACCESS \_ MASK-Datentyp** ist ein **DWORD-Wert,** der Standard-, spezifische und generische Rechte definiert. Diese Rechte werden in [*Zugriffssteuerungseinträgen (Access Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) verwendet und sind die primäre Möglichkeit, den angeforderten oder gewährten Zugriff auf ein Objekt anzugeben.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Hinweise

Die Bits in diesem Wert werden wie folgt zugeordnet.



| Bits             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Bestimmte Rechte. Enthält die Zugriffsmaske, die für den objekttyp spezifisch ist, der der Maske zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Standardrechte. Enthält die Standardzugriffsrechte des Objekts.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Zugriffssystemsicherheit (**ACCESS \_ SYSTEM \_ SECURITY**). Sie wird verwendet, um den Zugriff auf eine [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) anzugeben. Für diese Art von Zugriff muss der aufrufende Prozess über die **Berechtigung SE \_ \_ SICHERHEITSNAME** (Überwachung und Sicherheitsprotokoll verwalten) verfügen. Wenn dieses Flag in der Zugriffsmaske eines Zugriffs-ACE für die Überwachung festgelegt ist (erfolgreicher oder nicht erfolgreicher Zugriff), wird der SACL-Zugriff überwacht.<br/> |
| 25<br/>    | Maximal zulässig (**MAXIMUM \_ ALLOWED**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Generic all (**GENERIC \_ ALL**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Generische Ausführung (**GENERIC \_ EXECUTE**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Generischer Schreibvorgang (**GENERIC \_ WRITE**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Generischer Lese- (**GENERIC \_ READ**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

Bits mit Standardrechten (16 bis 23) enthalten die Standardzugriffsrechte des Objekts und können eine Kombination der folgenden vordefinierten Flags sein.



| bit           | Flag                         | Bedeutung                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Löschen Sie den Zugriff.<br/>                                                                                                                                                                                                                |
| 17<br/> | **\_READ-STEUERELEMENT**<br/> | Lesezugriff auf besitzer-, gruppen- und [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) des Sicherheitsdeskriptors.<br/> |
| 18<br/> | **\_SCHREIB-DAC**<br/>    | Schreibzugriff auf die DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **WRITE \_ OWNER**<br/>  | Schreibzugriff auf Besitzer.<br/>                                                                                                                                                                                                        |
| 20<br/> | **Synchronisieren**<br/>   | Synchronisieren sie den Zugriff.<br/>                                                                                                                                                                                                           |



 

Die folgenden Konstanten, die in Winnt.h definiert sind, stellen die spezifischen und Standardzugriffsrechte dar.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winnt.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zugriffssteuerung](access-control.md)
</dt> <dt>

[Grundlegende Access Control Strukturen](authorization-structures.md)
</dt> <dt>

[Zugriffsrechte und Zugriffsmasken](access-rights-and-access-masks.md)
</dt> <dt>

[**GENERISCHE \_ ZUORDNUNG**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

