---
title: RAS_PORT_STATISTICS Struktur (rassapi. h)
description: Die Struktur der RAS- \_ Port \_ Statistik meldet die Statistiken, die ein RAS-Server für einen verbundenen Port sammelt.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS Struktur-RAS
- PRAS_PORT_STATISTICS-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345299"
---
# <a name="ras_port_statistics-structure"></a>Struktur der RAS- \_ Port \_ Statistik

\[Die Struktur der **RAS- \_ Port \_ Statistik** wird ab Windows Vista nicht unterstützt.\]

Die Struktur der **RAS- \_ Port \_ Statistik** meldet die Statistiken, die ein RAS-Server für einen verbundenen Port sammelt. Der RAS-Server setzt die einzelnen Statistik Indikatoren zurück, wenn der Port verbunden ist. Aufrufen der [**rasadminportclearstatistics**](rasadminportclearstatistics.md) -Funktion, um das Zurücksetzen der Statistik Zähler durch den RAS-Server zu erzwingen.

Bei einem Port, der Teil einer Verbindung mit mehreren Links ist, stellt diese Struktur zwei Sätze von Statistiken bereit. Der erste Satz enthält die kumulativen Statistiken für alle Ports in der Verbindung. Diese Statistiken sind für alle Ports in der Verbindung identisch. Die zweite Gruppe enthält die Statistiken für nur diesen Port. Wenn der Port nicht Teil einer Verbindung mit mehreren Links ist, haben beide Statistik Sätze die gleichen Informationen. Um zu ermitteln, ob ein Port Teil einer Multilinkverbindung ist, überprüfen Sie das \_ multilinked-multilinked-Bit im **Flags** -Member der Struktur des Ports " [**RAS- \_ Port \_ 0**](ras-port-0-str.md) " des Ports.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwbytesxgetrennte**
</dt> <dd>

Gibt die Gesamtanzahl der Bytes an, die von der Verbindung übertragen werden.

</dd> <dt>

**dwbytesrcved**
</dt> <dd>

Gibt die Gesamtanzahl von Bytes an, die von der Verbindung empfangen werden.

</dd> <dt>

**dwframesxgetrennte**
</dt> <dd>

Gibt die Gesamtanzahl der von der Verbindung übertragenen Frames an.

</dd> <dt>

**dwframesrcved**
</dt> <dd>

Gibt die Gesamtanzahl der von der Verbindung empfangenen Rahmen an.

</dd> <dt>

**dwcrcerr**
</dt> <dd>

Gibt die Gesamtanzahl von CRC-Fehlern für die Verbindung an. CRC-Fehler werden dadurch verursacht, dass eine zyklische Redundanz Prüfung fehlgeschlagen ist. Ein CRC-Fehler gibt an, dass ein oder mehrere Zeichen im empfangenen Datenpaket beim Eintreffen gegartet wurden.

</dd> <dt>

**dwtimeouterr**
</dt> <dd>

Gibt die Gesamtzahl der Timeout Fehler für die Verbindung an. Timeout Fehler treten auf, wenn ein erwartetes Zeichen nicht rechtzeitig empfangen wird. Wenn dies der Fall ist, geht die Software davon aus, dass die Daten verloren gegangen sind und fordert, dass Sie erneut gesendet werden.

</dd> <dt>

**dwalignmenterr**
</dt> <dd>

Gibt die Gesamtanzahl der Ausrichtungsfehler für die Verbindung an. Ausrichtungsfehler treten auf, wenn ein empfangenes Zeichen nicht das erwartete Zeichen ist. Dies geschieht normalerweise, wenn ein Zeichen verloren geht oder ein Timeout Fehler auftritt.

</dd> <dt>

**dwhardwareoverrunerr**
</dt> <dd>

Gibt die Gesamtanzahl der Hardware Überlauf Fehler bei der Verbindung an. Diese Fehler geben an, wie oft der Sende Computer Zeichen schneller übertragen hat, als die Hardware des empfangenden Computers verarbeiten kann. Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.

</dd> <dt>

**dwframingerr**
</dt> <dd>

Gibt die Gesamtzahl der Rahmen Fehler für die Verbindung an. Ein Rahmen Fehler tritt auf, wenn ein asynchrones Zeichen mit einem ungültigen Start-oder Stoppbit empfangen wird.

</dd> <dt>

**dwbufferoverrunerr**
</dt> <dd>

Gibt die Gesamtanzahl der Pufferüberlauf Fehler für die Verbindung an. Ein Pufferüberlauf Fehler tritt auf, wenn der sendende Computer Zeichen schneller überträgt, als er von dem empfangenden Computer aufgenommen werden kann. Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.

</dd> <dt>

**dwbytesxmiteduncompressed**
</dt> <dd>

Gibt die Gesamtanzahl der Bytes an, die von der Verbindung nicht komprimiert werden.

</dd> <dt>

**dwbytesrcveduncompressed**
</dt> <dd>

Gibt die Gesamtanzahl der Bytes an, die von der Verbindung nicht komprimiert empfangen werden.

</dd> <dt>

**dwbytesxmitedcompressed**
</dt> <dd>

Gibt die Gesamtanzahl von Bytes an, die von der Verbindung komprimiert werden.

</dd> <dt>

**dwbytesrcvedcompressed**
</dt> <dd>

Gibt die Gesamtanzahl der Bytes an, die von der Verbindung komprimiert wurden.

</dd> <dt>

**dwportbytesxgetrennte**
</dt> <dd>

Gibt die Gesamtanzahl von Bytes an, die vom Port übertragen werden.

</dd> <dt>

**dwportbytesrcved**
</dt> <dd>

Gibt die Gesamtanzahl von Bytes an, die vom Port empfangen wurden.

</dd> <dt>

**dwportframesxgetrennte**
</dt> <dd>

Gibt die Gesamtanzahl der vom Port übertragenen Frames an.

</dd> <dt>

**dwportframesrcved**
</dt> <dd>

Gibt die Gesamtanzahl von Frames an, die vom Port empfangen werden.

</dd> <dt>

**dwportcrcerr**
</dt> <dd>

Gibt die Gesamtanzahl von CRC-Fehlern auf dem Port an. CRC-Fehler werden dadurch verursacht, dass eine zyklische Redundanz Prüfung fehlgeschlagen ist. Ein CRC-Fehler gibt an, dass ein oder mehrere Zeichen im empfangenen Datenpaket beim Eintreffen gegartet wurden.

</dd> <dt>

**dwporttimeouterr**
</dt> <dd>

Gibt die Gesamtzahl der Timeout Fehler für den Port an. Timeout Fehler treten auf, wenn ein erwartetes Zeichen nicht rechtzeitig empfangen wird. Wenn dies der Fall ist, geht die Software davon aus, dass die Daten verloren gegangen sind und fordert, dass Sie erneut gesendet werden.

</dd> <dt>

**dwportalignmenterr**
</dt> <dd>

Gibt die Gesamtanzahl der Ausrichtungsfehler für den Port an. Ausrichtungsfehler treten auf, wenn ein empfangenes Zeichen nicht das erwartete Zeichen ist. Dies geschieht normalerweise, wenn ein Zeichen verloren geht oder ein Timeout Fehler auftritt.

</dd> <dt>

**dwporthardwareoverrunerr**
</dt> <dd>

Gibt die Gesamtanzahl der Hardware Überlauf Fehler auf dem Port an. Diese Fehler geben an, wie oft der Sende Computer Zeichen schneller übertragen hat, als die Hardware des empfangenden Computers verarbeiten kann. Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.

</dd> <dt>

**dwportframingerr**
</dt> <dd>

Gibt die Gesamtzahl der Rahmen Fehler an dem Port an. Ein Rahmen Fehler tritt auf, wenn ein asynchrones Zeichen mit einem ungültigen Start-oder Stoppbit empfangen wird.

</dd> <dt>

**dwportbufferoverrunerr**
</dt> <dd>

Gibt die Gesamtanzahl der Pufferüberlauf Fehler auf dem Port an. Ein Pufferüberlauf Fehler tritt auf, wenn der sendende Computer Zeichen schneller überträgt, als er von dem empfangenden Computer aufgenommen werden kann. Wenn dieses Problem weiterhin besteht, verringern Sie die Verbindungs Rate für Bit/s auf dem Client.

</dd> <dt>

**dwportbytesxmiteduncompressed**
</dt> <dd>

Gibt die Gesamtanzahl der Bytes an, die vom Port nicht komprimiert gesendet werden. Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig. Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.

</dd> <dt>

**dwportbytesrcveduncompressed**
</dt> <dd>

Gibt die Gesamtanzahl der Bytes an, die vom Port nicht komprimiert empfangen werden. Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig. Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.

</dd> <dt>

**dwportbytesxmitedcompressed**
</dt> <dd>

Gibt die Gesamtanzahl von Bytes an, die vom Port komprimiert werden. Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig. Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.

</dd> <dt>

**dwportbytesrcvedcompressed**
</dt> <dd>

Gibt die Gesamtanzahl der Bytes an, die vom Port komprimiert werden. Wenn der Port Teil einer Verbindung mit mehreren Links ist, ist dieser Member ungültig. Verwenden Sie stattdessen die Komprimierungs Statistik für die Verbindung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**RAS- \_ Port \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**Rasadminakzeptnewconnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**Rasadminconnectionhangupnotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**Rasadminportclearstatistics**](rasadminportclearstatistics.md)
</dt> <dt>

[**Rasadminportgetinfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





