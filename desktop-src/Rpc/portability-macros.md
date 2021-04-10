---
title: Portabilitäts Makros (RPC. h)
description: Die RPC-Tools erreichen die Unabhängigkeit von Modellen, aufrufen und Benennungs Konventionen durch Zuordnen von Datentypen und Funktions Rückgabe Typen in den generierten Stubdateien und Header Dateien mit Definitionen, die für die einzelnen Plattformen spezifisch sind.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- Portabilitäts Makros RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "103961083"
---
# <a name="portability-macros"></a>Portabilitäts Makros

Die RPC-Tools erreichen die Unabhängigkeit von Modellen, aufrufen und Benennungs Konventionen durch Zuordnen von Datentypen und Funktions Rückgabe Typen in den generierten Stubdateien und Header Dateien mit Definitionen, die für die einzelnen Plattformen spezifisch sind. Mit diesen Makro Definitionen wird sichergestellt, dass alle Datentypen und Funktionen, die die Bezeichnung " **\_ \_ weit** " erfordern, als Objekte angegeben werden.

In der folgenden Abbildung werden die Makro Definitionen veranschaulicht, die der Mittelwert Compiler für Funktionsaufrufe zwischen RPC-Komponenten anwendet:

![Das Diagramm, in dem die Makro Definitionen der Mittel l für Funktionsaufrufe angewendet werden.](images/prog-a29.png)

RPC-Makros werden wie folgt definiert.



| Definition    | BESCHREIBUNG                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_RPC- \_ API  | Wird auf Aufrufe angewendet, die vom Stub für die Benutzeranwendung ausgeführt werden. Beide Funktionen befinden sich in demselben ausführbaren Programm.                                       |
| \_\_RPC- \_ weit  | Wird auf die standardmäßige Makro Definition für Zeiger angewendet. Diese Makro Definition sollte als Teil der Signatur aller vom Benutzer bereitgestellten Funktionen angezeigt werden. |
| \_\_RPC- \_ Stub | Wird auf Aufrufe der Lauf Zeit Bibliothek auf den Stub angewendet. Diese Aufrufe können als privat angesehen werden.                                                 |
| \_\_RPC- \_ Benutzer | Gilt für Aufrufe, die von der Lauf Zeit Bibliothek für die Benutzeranwendung durchgeführt werden. Diese überschreiten die Grenzen zwischen einer DLL und einer Anwendung.                   |
| RPC- \_ Eintrag    | Gilt für Aufrufe, die von der Anwendung oder dem Stub für die Lauf Zeit Bibliothek durchgeführt werden. Diese Makro Definition wird auf alle RPC-Lauf Zeitfunktionen angewendet.           |



 

Zum ordnungsgemäßen verknüpfen mit den Microsoft RPC-Laufzeitbibliotheken,-Stub-und-Unterstützungs Routinen müssen einige benutzerdefinierte Funktionen diese Makros ebenfalls in die Funktionsdefinition einschließen. Verwenden Sie die Makro- **\_ \_ RPC- \_ API** , wenn Sie die der Speicherverwaltung zugeordneten Funktionen, benutzerdefinierte Bindungs Handles und das Attribut "über **tragen \_ als** " definieren und den RPC-Makro **\_ \_ \_ Benutzer** verwenden, wenn Sie die dem Kontext Handle zugeordnete Kontext-Lauf Zeit Routine definieren. Geben Sie die Funktionen wie folgt an:

<dl> <dt>

<span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC- \_ Benutzer- *mittlere \_ Benutzer* Zuordnungen \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_\_ *\_ Benutzer* kostenlos für RPC-Benutzer \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC \_ - *benutzertypbindung* \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_Aufheben der Bindung des RPC- \_ Benutzer *handtyps* \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC \_ - *Benutzertyp* \_ zu \_ lokal
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC \_ - *Benutzertyp* \_ aus \_ lokalem
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC- \_ Benutzertyp \_ in \_ xmit (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC \_ - *Benutzertyp* \_ von \_ xmit (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC \_ - *Benutzertyp* \_ Free \_ lokal
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC \_ - *Benutzertyp* \_ freie \_ inst (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC \_ - *Benutzertyp*" \_ freier \_ xmit (...)"
</dt> <dd></dd> <dt>

<span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC- \_ Benutzer Kontext- \_ Rundown (...)
</dt> <dd></dd> </dl>

> [!Note]  
> Alle Zeiger Parameter in diesen Funktionen müssen mit dem gesamten RPC- **\_ \_ RPC \_**-Typ angegeben werden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



 

 





