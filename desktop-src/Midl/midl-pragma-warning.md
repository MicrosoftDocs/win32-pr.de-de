---
title: midl_pragma Warning-Attribut
description: Verwenden Sie die Option "Mittell \_ -pragma-Warnung", um das Verhalten für die Warnmeldung von mittlerer l zur Kompilierzeit vorübergehend
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma Warning-Attribut, Mittel l
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857224"
---
# <a name="midl_pragma-warning-attribute"></a>Mittel l- \_ pragma-Warnungs Attribut

Verwenden Sie die Option " **Mittell- \_ pragma-Warnung** ", um das Verhalten für die Warnmeldung von mittlerer l zur Kompilierzeit vorübergehend

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Option "Warnung" \_* 
</dt> <dd>

Die Option "Warnung" kann eines der folgenden sein: "deaktivieren", "aktivieren", "Standard".

</dd> <dt>

*Nachrichten \_ Liste* 
</dt> <dd>

Eine durch Leerzeichen getrennte Liste von Nachrichtennummern.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Pragma kann wie ein C-Compiler-Pragma verwendet werden. Das heißt, dass Sie das Standardverhalten für eine bestimmte Mittell-Warnung deaktiviert, aktiviert oder zurückgibt.

## <a name="examples"></a>Beispiele

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




