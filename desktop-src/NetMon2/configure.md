---
description: Konfiguriert den Experten innerhalb der Experten-dll.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Rückruffunktion konfigurieren (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357730"
---
# <a name="configure-callback-function"></a>Rückruffunktion konfigurieren

Die Funktion **configure** konfiguriert den Experten innerhalb der Experten-dll.

Der Experte muss die **configure** -Funktion implementieren. Beim Empfang des Funktions Aufrufes zeigt der Experte ein Dialogfeld an, in dem der Benutzer beliebige konfigurierbare Elemente ändern kann.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexpertkey* \[ in\]
</dt> <dd>

Eindeutige expertenkennung.

Der eindeutige Bezeichner wird an alle expertenspezifischen Netzwerkmonitor Funktionen zurückgegeben. Beachten Sie, dass es sich bei dem Bezeichner möglicherweise nicht um denselben expertenschlüssel handelt wie der, der an die Funktion [**Run (ausführen**](run.md) ) Speichern Sie den expertenschlüssel nicht aus dem **configure** -Befehl.

</dd> <dt>

*ppconfig* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine " [**expertenconfig**](expertconfig.md) "-Struktur beim Eintrag.

Nach einem erfolgreichen beenden enthält die referenzierte [**expertenkonfigurationsstruktur**](expertconfig.md) die neuen Konfigurationsdaten.

</dd> <dt>

*pexpertstartupinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf das Erfassungs Element mit Fokus, wenn der Experte gestartet wurde.

</dd> <dt>

*StartupFlags* \[ in\]
</dt> <dd>

Die Flags, die angeben, wie der Experte den *pexpertstartupinfo* -Parameter verwenden soll. Das einzige Flag, das **als expertenstartflag definiert ist, ist die \_ Verwendung von \_ \_ \_ Startdaten für \_ \_ \_ Konfigurations \_ Daten**. Das-Flag gibt an, dass der Experte den *pexpertstartupinfo* -Parameter anstelle des übergebenen *ppconfig* -Parameters verwendet. In der Regel legen Sie das-Flag fest, wenn Sie den Experten über ein Kontextmenü starten.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster. Verwenden Sie das Handle, um ein Dialogfeld zu öffnen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn eine aktuelle Konfiguration vorhanden ist), ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Netzwerkmonitor Ruft die **configure** -Funktion mit der aktuellen Konfiguration des Experten auf, sofern eine vorhanden ist. Der Experte zeigt ein Dialogfeld an, in dem Sie beliebige konfigurierbare Elemente ändern können.

Wenn *ppconfig* in übergeben wird und Netzwerkmonitor keine Konfiguration für den angegebenen Experten gespeichert hat, kann der Parameterwert **null** sein. In diesem Fall geht die **configure** -Funktion von hart codierten Standardwerten aus (oder verwendet die Startinformationen), um das Dialogfeld zu öffnen.

Die Konfigurationsdaten können auch **null** sein, wenn die Funktion " **configure** " zurückgegeben wird, und es wurde ein **null** -Wert zurückgegeben. Diese Situation tritt auf, wenn Netzwerkmonitor keinen gespeicherten Standardwert besitzt, und der Benutzer auf **Abbrechen** drückt.

Der Anfang der Datenstruktur " [**expertconfig**](expertconfig.md) " enthält einen privaten Abschnitt, in dem die Informationen zur Struktur Größe gespeichert werden. Die Größe der **expertenkonfigurationsstruktur** sollte die reservierte **DWORD** -Länge enthalten, die am Anfang der Struktur angezeigt wird. Wenn die Konfigurationsdaten z. b. 20 Bytes Speicherplatz benötigen, müssen Sie 24 Bytes zum Speichern der Daten zuordnen. Wenn ein *ppconfig* -Wert **null** ist, ruft die **configure** -Funktion [**die Funktion "-Funktion"**](expertallocmemory.md) auf, um eine neue Konfiguration zuzuordnen, die die richtige Größe hat. Wenn der Puffer nicht ausreichend ist, um die Expertendaten aufzunehmen, sollte der Experte die Funktion " [**expertrebelegcmemory**](expertreallocmemory.md) " anrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




