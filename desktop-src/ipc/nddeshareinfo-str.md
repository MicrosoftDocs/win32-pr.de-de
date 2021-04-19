---
description: Enthält DDE-Freigabe Attribute, die vom NetDDE-Freigabe Datenbank-Manager (DSDM) verwaltet werden.
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Ndbeshareingefo-Struktur (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364197"
---
# <a name="nddeshareinfo-structure"></a>Ndbeshareingefo-Struktur

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Enthält DDE-Freigabe Attribute, die vom NetDDE-Freigabe Datenbank-Manager (DSDM) verwaltet werden. Die Sicherheits Beschreibung, die den einzelnen DDE-Freigaben zugeordnet ist, wird nicht über diese Struktur, sondern über bestimmte Funktionen aufgerufen. Die NetDDE-DSDM-API akzeptiert diese Struktur für Set-Funktionen. für Get-Funktionen gibt die DSDM die Struktur, die in den angegebenen Puffer gepackt ist, zusammen mit den Daten zurück, auf die von den Membern **lpszsharename**, **lpszapptopiclist** und **lpszitemlist** verwiesen wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**lrevision**
</dt> <dd>

Die Revisions Ebene der **nddebug-Info** -Struktur. Derzeit ist die Revisions Ebene 1.

</dd> <dt>

**lpszsharename**
</dt> <dd>

Der Name der Freigabe. Diese Zeichenfolge darf nicht größer sein als die maximale Anzahl von \_ ndde ShareName-Zeichen.

</dd> <dt>

**lsharetype**
</dt> <dd>

Ein oder mehrere DDE-Freigabe Typen. Dieser Member kann eine Kombination der folgenden unterstützten DDE-Freigabe Typen sein.



| Freigabetyp                                                                                                                                                                                                                           | Bedeutung                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**Freigabe \_ \_Neuer**</dt> <dt>0x02</dt> eingeben </dl>          | Die Freigabe enthält ein OLE-Anwendungs-/Topic-Paar.<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**Freigabe \_ Geben Sie \_ Alter**</dt> <dt>0x01</dt> ein. </dl>          | Die Freigabe enthält ein DDE-Anwendungs-/Topic-Paar.<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**Freigabe \_ \_Typstatic**</dt> <dt>0x04</dt> </dl> | Die Freigabe enthält ein statisches Anwendungs-/Topic-Paar.<br/> |



 

</dd> <dt>

**lpszapptopiclist**
</dt> <dd>

Ein Zeiger auf einen Puffer, der NULL-terminierte Zeichen folgen für das DDE, OLE und statische Anwendungs-/Topic-Paare enthält. Der Puffer sollte das folgende Format aufweisen:

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**"ssharedflag"**
</dt> <dd>

Wenn dieser Member **false** ist, lässt die DDE-Freigabe nicht zu, dass Remote Benutzer mithilfe von DDE kommunizieren. Lokale Benutzer können jedoch weiterhin über die DDE-Freigabe kommunizieren. Lokale Client Links werden immer impliziert, wenn die zugehörige DACL Zugriff gewährt.

</dd> <dt>

**Dienst**
</dt> <dd>

Wenn dieser Member festgelegt ist, überprüft die DDE-Freigabe nicht, ob der aktuelle Benutzer Sie als vertrauenswürdig festgelegt hat, bevor die DDE-Kommunikation zugelassen wird.

</dd> <dt>

**"sstartappflag"**
</dt> <dd>

Wenn dieser Member festgelegt ist und die Freigabe vertrauenswürdig ist, um Anwendungen zu starten, versucht NetDDE, die von **lpszapptopiclist** angegebene Anwendung zu starten, wenn er nicht anfänglich eine DDE-Konversation mit der Anwendung startet.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Wenn NetDDE eine Anwendung zum Initiieren einer DDE-Konversation startet, wird dieser Wert über den *nCmdShow* -Parameter der [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion an die Anwendung gesendet. Es definiert den bevorzugten Modus, in dem das Anwendungsfenster angezeigt werden soll. Dieser Parameter ist nur dann von Bedeutung, wenn " **f startappflag** " aktiv ist. Der angemeldete Benutzer, in dessen Kontext die Anwendung gestartet wurde, kann diese Option auch überschreiben, wenn die Freigabe zum vertrauenswürdigen Status herauf gestuft wird. Der Standardwert für diesen Member ist "SW \_ showmaximized".

</dd> <dt>

**qmodifyid**
</dt> <dd>

Eine 8-Byte-Seriennummer, die die Änderungs Seriennummer der DDE-Freigabe angibt. Jedes Mal, wenn die DDE-Freigabe durch einen [**nddesharesetinfo**](nddesharesetinfo.md) -oder einen [**nddesetsharesecurity**](nddesetsharesecurity.md) -Aufruf geändert wird, werden diese Werte geändert.

</dd> <dt>

**cnumitems**
</dt> <dd>

Die Anzahl der in **lpszitemlist** aufgeführten Elemente. Wenn **cnumitems** gleich 0 (null) ist, ist **lpszitemlist** leer, und die Freigabe Informationen und die zugehörige Sicherheits Beschreibung gelten für alle Elemente, die von der zugehörigen Anwendung bedient werden.

</dd> <dt>

**lpszitemlist**
</dt> <dd>

Ein Zeiger auf einen Puffer mit null-terminierten Zeichen folgen, die die Elemente angeben, die von der Client Anwendung in einer DDE-Transaktion angefordert oder gestartet werden können. Wenn keine Elemente aufgelistet werden, kann die DDE-Freigabe alle Elemente verwenden. Die Anzahl der Elemente in der Liste muss der Anzahl der **cnumitems** entsprechen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Netzwerk-DDE-Strukturen](network-dde-structures.md)
</dt> <dt>

[**Ndde setsharesecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**Nddesharesetinfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

